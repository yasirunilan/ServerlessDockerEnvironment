# serverless-docker
docker image for serverless development


## Build the image

```
docker build -t yasi92/serverless-dev .
```

## Run the image

```
# run the image to get a shell
docker run -it --name svless -v ~/projects/svless:/home/svless -p 8000:8000 yasi92/serverless-dev /bin/bash
```

```
# run the image to execute a sls command and delete the container
docker run --rm -v ~/projects/svless:/home/svless yasi92/serverless-dev
```

## Pass in the AWS Credentials to the container at runtime

```
# pass the AWS credential env vars. from host
docker run -it --name svless \
           -v ~/projects/svless:/home/svless \
           -e AWS_ACCESS_KEY_ID \
           -e AWS_SECRET_ACCESS_KEY \
           yasi92/serverless-dev /bin/bash
```

OR

```
# pass the AWS credentials file from host
docker run -it --name svrless \
           -v ~/projects/svrless:/home/svrless \
           --env-file ~/.aws/credentials \
           rupakg/serverless-docker /bin/bash
```
Then, run ```aws configure``` and pass in the AWS credentials.
