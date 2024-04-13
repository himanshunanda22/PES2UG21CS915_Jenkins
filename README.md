# Building C++ Project with Jenkins in Docker

This repository demonstrates how to set up a Jenkins environment within a Docker container to build a simple C++ project.

## Dockerfile

The Dockerfile contains instructions for building a Docker image based on the official Jenkins LTS image (`jenkins/jenkins:lts`). It installs the necessary packages (`make` and `g++`) to build C++ projects. Here's a breakdown of the Dockerfile:

```Dockerfile
FROM jenkins/jenkins:lts

USER root

RUN apt-get update && apt-get install -y make g++

USER jenkins
```
