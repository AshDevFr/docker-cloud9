Cloud9 v3 Dockerfile
=============

This repository contains Dockerfile of Cloud9 IDE for Docker's automated build published to the public Docker Hub Registry.

# Base Docker Image
[kdelfour/supervisor-docker](https://registry.hub.docker.com/u/kdelfour/supervisor-docker/)

# Installation

## Install Docker.

(alternatively, you can build an image from Dockerfile: docker build -t="ashdevfr/docker-cloud9" github.com/ashdevfr/docker-cloud9)

## Usage

    docker run -it -d -p 80:80 ashdevfr/cloud9-docker

You can add a workspace as a volume directory with the argument *-v /your-path/workspace/:/workspace/* like this :

    docker run -it -d -p 80:80 -v /your-path/workspace/:/workspace/ ashdevfr/cloud9-docker

## Build and run with custom config directory

Get the latest version from github

    git clone https://github.com/AshDevFr/docker-cloud9.git
    cd cloud9-docker/

Build it

    sudo docker build --force-rm=true --tag="$USER/cloud9-docker:latest" .

And run

    sudo docker run -d -p 80:80 -v /your-path/workspace/:/workspace/ $USER/cloud9-docker:latest

Enjoy !!    

Thanks to kdelfour (github.com/kdelfour/cloud9-docker)
