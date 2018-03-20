# DockerTests

Example hello-world Java application developed using Dropwizard and ran from a Docker container

## Build and Execution

To build the Dropwizard "fat jar", run the following command:

```
mvn clean package
```

To create the docker container, run:

```
mvn docker:build
```

Then run the docker image:

```
docker run -it -p 8090:8090 -p 8091:8091 hello-world:0.0.1-SNAPSHOT
```

You can then send a message to the service using:

```
curl -s 'http://localhost:8090/hello-world'
```

## Credits

Followed these two tutorials:

Dropwizard Getting Started
http://www.dropwizard.io/0.9.1/docs/getting-started.html

Building a Dropwizard Microservice with Docker and Maven
https://blog.philipphauer.de/building-dropwizard-microservice-docker-maven/