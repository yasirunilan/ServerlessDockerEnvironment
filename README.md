# serverless #

[![Build Status](https://travis-ci.org/yasirunilan/ServerlessDockerEnvironment.svg?branch=master)](https://travis-ci.org/yasirunilan/ServerlessDockerEnvironment)

A [docker image](https://hub.docker.com/r/yasi92/serverless-dev/) for running [serverless](https://serverless.com) commands.

This is a docker image for serverless application development.

## Example ##

```
$ docker pull yasi92/serverless-dev
$ docker run --rm yasi92/serverless-dev --version
```

Included packages from base image:

- [aws-cli](https://github.com/aws/aws-cli).

## Additional packages ##

- Nodejs 6.x
- Serverless cli
