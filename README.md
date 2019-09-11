# Docker + Node "Hello World" Example

This repository gives you a quick introduction to getting docker running with Node. It is intended for the Docker beginner.

## Setup

First, checkout this project locally and then follow these steps:

1. Install the [Docker for Windows](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe).
2. Start a [Quickstart Terminal](https://docs.docker.com/v17.09/docker-for-windows/install/#install-docker-for-windows)session (see the getting started guide).
3. Build the Docker image: `docker build -t hello-world .`
4. Run the image in a container: `docker run -d -p 4001:4000 hello-world`
  - The `-d` flag says to run the container in the background (daemon mode).
  - The `-p` flag maps port 4000 from the container to port 4001 on the docker machine.
5. View your new container: `docker ps -a`
6. Check the logs for your container: `docker logs <container-id>`
7. Check the port of the container: `docker port <container-id>`
8. Open the app running on the docker machine: `open http://localhost:4001`



## Notes & Tips

- If you make changes to your application, you will need to rebuild your image and restart your container.
- View logs for a docker container: `docker logs <container-id>`
- List the running containers: `docker ps -a`
- List all local images: `docker images`
- Remove an image: `docker rmi <image-id>`
- Remove a container: `docker rm <container-id>`