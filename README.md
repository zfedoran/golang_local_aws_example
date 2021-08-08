# Simple golang service with local AWS services

An example to show how to setup AWS local development environment using golang aws-sdk-v2 and localstack.

In this example, there are 2 AWS components, S3 and SQS. Both components are run locally without communicating with the external AWS services.  

## 1.Prerequisites
Need to install:
  - Docker and Docker Compose

## 2.How to run
- Start docker compose: `docker-compose up`
- Use `https://github.com/aaronshaf/dynamodb-admin` if you need to view / update dynamodb data