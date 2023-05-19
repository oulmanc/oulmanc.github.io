---
layout: post
title: "Containerize Everything With Docker"
date: 2023-05-19 12:00:00 -0500
categories: docker
tags: docker linux
---

![docker](https://carlos.oulman.net/wp-content/uploads/2022/03/docker_gfx.jpg)

If you’ve been in the world of technology long enough, you’ll probably be familiar with the concept of virtual machines. VM’s are an awesome technology that allows us to do some really neat stuff but there’s a new kid in town and the name’s Docker. If you haven’t heard of Docker, think virtualization but for software rather than an entire computer. Docker containers take all the dependencies needed to run something and put them all together in a nice little package. We won’t be going super in-depth about what Docker is or how to use it but what we will do is get it set up and install Docker Compose.

Before we can get Docker setup, we’ll first need an environment to run it in. In some of my other tutorials, I have gone with Debian but I’ve recently made the switch to Ubuntu as it’s based on Debian and tends to offer more support. If you’re setting up a new environment, it’s a good idea to review some best practices before moving forward. This is especially important if you’ll be using this as a production server.

Because documentation will change over time, let’s use the official instructions from Docker. Those can be found [here](https://docs.docker.com/engine/install/ubuntu/). Let’s assume you are starting with a fresh image, you can skip the uninstallation section but running those commands won’t hurt anything if Docker isn’t already installed. There are a few methods for getting Docker set up but I recommend installing Docker using the repository. After you have the repository set up, you can install the Docker Engine using `apt`. Unless you have a specific need, installing the latest stable version is the best option. When the installation is done, run the `hello-world image` to verify Docker is working.

So we now have Docker on our system and we’re ready to start spinning up Docker containers. What I have found is that while you can use Docker commands to run images, if you are running an image that requires some additional variables, it’s can be a bit difficult to get them set up. Welcome, Docker Compose. Docker Compose utilizes a YAML file to store the variable for your container then, you can just run `sudo docker-compose up` to start your container. By default, Docker Compose isn’t installed so let’s take care of that now.

Again, as documentation will change on this process over time, the official instructions can be found [here](https://docs.docker.com/compose/install/). Since we are using Linux, you’ll want to follow the setup instructions under the Linux tab. Start by downloading the current stable version. Next, you will need to adjust the executable permissions. With both those steps done, you should be set to test the installation. If the version comes back, you’re all set.

Now that we have both Docker and Docker Compose setup, we can start running our docker containers. If there is something you want to run on your server, most likely there is a Docker image for it. Check out [Docker Hub](https://hub.docker.com/) for more information. In a future tutorial, we’ll look at getting Portainer set up so we can manage our Docker Containers using a web GUI.