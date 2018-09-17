# Sambda
Run the simplest possible AWS Lambda function locally.

## Requirements
* [Python](https://www.python.org/downloads/)
* [AWS CLI](https://aws.amazon.com/cli/) 
* [AWS SAM CLI](https://docs.aws.amazon.com/lambda/latest/dg/test-sam-cli.html)
* [Docker](https://www.docker.com/community-edition)

## How to use
```bash
sam local invoke -e event.json
```