---
title: "Using AWS Lambda Powertools for Python"
date: 2025-03-20
tags: ["aws", "python", "lambda"]
---

AWS Lambda Powertools is a set of utilities that help simplify the development of serverless applications in AWS. In this post, we will explore how to use Powertools for logging, tracing, and metrics.

To start using AWS Lambda Powertools, you need to install the package:

```bash
pip install aws-lambda-powertools
```

Here’s an example of using the Logger utility for structured logging:
```python
from aws_lambda_powertools import Logger

logger = Logger(service="my-service")

@logger.inject_lambda_context
def lambda_handler(event, context):
    logger.info("Lambda function started")
    return {"statusCode": 200, "body": "Hello, World!"}

```

This simple setup enables better observability for your Lambda functions.