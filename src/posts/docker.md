---
layout: layouts/post.njk
title: Docker
date: 2019-09-18T12:46:13.983Z
tags:
  - docker
---
# Docker ?

Docker is platform which helps us to ship, build and deploy application. It provides us containerization platform which is different then virtual machine. A VM (Virtual Machine) is whole OS which sits on top of a host OS but a container is just a collection of things which we need. 



`docker run -it -d` Command docker run will pass a message to docker client with command -it which means to become interactive and -d which means run it in daemon mode. `docker exec -it cfc5986d653d bash` This command will execute a command in a provided container id or container name. It will only work if our container is running and not stopped. To stop our docker container we have to run docker stop [containerId]. We can see list of docker containers which are running by command `docker ps` but it will not show the container which are not running currently. To list all the container which both are running or not we have to provide extra argument `-a` to command `docker ps`, which will make `docker ps -a`.





To list all the images we have used or pulled in our local machine we can use the command `docker images` and to search an image from command line we can hit `docker search [keyword]` which will list all matching images found in docker hub registry.

`docker kill [containerid] ` to kill any container which are refusing to shut down. How kill differs from stop is that `stop` will wait and shut down gracefully where kill will just stop everything and it doesn’t care or know anything about word `graceful`.

`docker rm [containerid]` to remove container from machine and `docker rmi [imageid]` to remove docker image from local machine.



# Docker image and docker container?

Docker image can be understood, at least for me as a class and docker container are an instance of it. I am OOP lover and understanding this way helps me to understand it visually and conceptually. Like a class can have multiple instances of object similarly a image will have multiple instances which can called as container.





# Dockerfile

A dockerfile is simple plain text file where we write about how our image will be created. It is simple text file so it can be open and edited by any text editor which can handle mime text/plain. I think every editor does that even photoshop. In our dockerfile we will write instructions to build image by using some special command which is understood by only docker and not photoshop.

Some command i remember are.	

FROM, ADD, RUN, WORKDIR, CMD, ENV etc.

FROM  - will pull image from docker hub or your private/public repository

ADD - Will add files/folders to image/container

RUN - Will run provided command which can be understood by OS

WORKDIR -  will set our work directory

CMD - same like run but takes args, ENV - ?



# Remove all containers running and not running 

sudo docker rm -f $(sudo docker ps -a -q)  // Removes all container


# Mount

   docker run -it -v /home/samundra/Pictures:/app -d keyboard 

# Volume

 docker run -it --mount source=test,target=/app -d keyboard
