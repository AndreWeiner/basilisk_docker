# Build Basilisk Docker images

This repository contains Dockerfiles to create images of the [Basilisk](http://basilisk.fr/) framework. Many of the commands come from [this](https://github.com/sgllewellynsmith/basilisk-docker) Github repo by [sgllewellynsmith](https://github.com/sgllewellynsmith).

## Dockerfiles

The images are currently based on Ubuntu 18.04. Every images in the following list suits a different purpose.

- *Dockerfile.minimal*: minimal installation of Basilisk without Python interface and Bview

To build an image based on a Dockerfile, the command looks as follows:

```
docker build -t registry_user_name/basilisk:version-tag -f Dockerfile.version .
```
Note that the registry name is useful if you want to push your image to a registry like Dockerhub, but you can also omit the prefix. A concrete example to build the minimal version of Basilisk could look like:
```
docker build -t andreweiner/basilisk:20-11-19 -f Dockerfile.minimal .
```
