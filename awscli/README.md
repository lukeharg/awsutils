# AWS CLI
Running the AWS CLI in a container with a clean Python environment

## Prerequisites
- An AWS account
- Docker installed on your local machine

## Getting started
### Credential file setup
Create a credential file (with appropriate permissions) on your local machine.
```
touch ~/.aws/awscreds.sh
```
The file should contain something like this.
```
AWS_ACCESS_KEY_ID=SOMEACCESSKEYID
AWS_SECRET_ACCESS_KEY=SOMESECRETACCESSKEYWHICHISLONGER
AWS_DEFAULT_REGION=us-east-1
````

### Installation
```
docker build -t lukeharg/awscli .
```

### Test the CLI by listing all your S3 buckets.
```
docker run --rm --env-file ~/.aws/awscreds.sh lukeharg/awscli s3 ls
```

## Todo
- Maybe create a script file for Linux and Windows instead of running the full command.


