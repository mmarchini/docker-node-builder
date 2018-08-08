# node-builder Docker images

[![dockeri.co](https://dockeri.co/image/mmarchini/node-builder)](https://registry.hub.docker.com/mmarchini/node-builder/)

[![GitHub issues](https://img.shields.io/github/issues/mmarchini/docker-node-builder.svg "GitHub issues")](https://github.com/mmarchini/docker-node-builder/issues/)
[![GitHub PRs](https://img.shields.io/github/issues-pr/mmarchini/docker-node-builder.svg "GitHub PRs")](https://github.com/mmarchini/docker-node-builder/pulls/)
[![GitHub stars](https://img.shields.io/github/stars/mmarchini/docker-node-builder.svg "GitHub stars")](https://github.com/mmarchini/docker-node-builder)

Docker images with the toolchain required to build Node.js on Linux.

## Usage

```
# Get Node.js source code
git clone https://github.com/nodejs/node
cd node/

# Download the image.
docker pull mmarchini:node-builder
# Run the container
docker run -v $(pwd):/node mmarchini:node-builder

# If you want to use clang, use the image below
docker pull mmarchini/node-builder:clang
docker run -v $(pwd):/node mmarchini/node-builder:clang
```

## Note for non-Linux Users

You'll be able to build Node.js with these images, but the resulting binary
won't work on OS X or Windows. You'll still be able to run the binary inside
the container if you want though.
