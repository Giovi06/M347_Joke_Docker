# This Dockerfile builds a container image for a Go application that provides jokes.
# It uses the golang:1.19-alpine base image and sets the working directory to /usr/src/app.
# The go.mod file is copied and the dependencies are downloaded and verified using go mod download and go mod verify.
# The JokeProvider.go file is copied and the application is built using go build.
# The resulting binary is placed in /usr/local/bin/app.
# The container runs the application by default when started.

FROM golang:1.19-alpine

WORKDIR /usr/src/app

COPY go.mod ./
RUN go mod download && go mod verify

COPY JokeProvider.go .
RUN go build -v -o /usr/local/bin/app ./...

CMD ["app"]