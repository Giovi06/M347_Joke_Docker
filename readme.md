# Guide

## Pull Images from Docker Hub Images

docker pull giovi06/m347-joke:joke-consumer-py-347

docker pull giovi06/m347-joke:joke-provider-go-347

## OR create Images

#### From Host directory to the JokeProviderGo

$ cd M347_LB02_JokeProviderGo

$ docker build -t joke-provider-go .

##### If you want to test the server:

$ docker run -it --rm -p 3001:3001 --name provider-go joke-provider-go

#### From Host directory to the JokeConsumerPython

$ cd M347_LB02_JokeConsumerPython

$ docker build -t joke-consumer-python .

## Build the Containers with docker-compose

#### From Host directory:

$ docker-compose up
