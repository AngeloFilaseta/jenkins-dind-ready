# jenkins-dind-ready

## Motivations 
When it comes to Docker, [Jenkins documentation](https://www.jenkins.io/doc/book/installing/docker/) states:


> There are several Docker images of Jenkins available.  
> Use the recommended official jenkins/jenkins image from the Docker Hub repository. This image contains the current Long-Term Support (LTS) release of Jenkins, which is production-ready. However, this image doesn’t contain Docker CLI, and is not bundled with the frequently used Blue Ocean plugins and its features. To use the full power of Jenkins and Docker, you may want to go through the installation process described below.

This repository purpose is to reduce the process of downloading and running Jenkins in Docker
(while still having access to a [DinD](https://hub.docker.com/_/docker) daemon) to a single command.

## Executing
1. Starts all containers using the following command. `-d` means that the containers run in the background, not locking the terminal from where the command was executed.
```shell
docker compose up -d
```

2. Enter http://localhost:8080/ and proceed like you would normally do in a plain Jenkins installation.