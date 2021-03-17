# Question
##### Sharing the docker daemon
Now that you know the inception of docker we are going to learn, how to share your host daemon to create more dockers, instead of doing docker in docker. So the task here is to create  a dockerfile, from alpine image base, and install the docker in it, but what we want is that when you execute the docker run command, you share the docker daemon with -v option, so after that you can start creating more containers from this containers.

###### Answer:
Dockerfile
<pre>
FROM alpine:3.11

RUN apk update

RUN apk add --update docker
	</pre>


#### Command instruction:
Build the image and run that image
<pre>
docker build -t docker-alpine .
docker run -it -v /var/run/docker.sock:/var/run/docker.sock:rw docker-alpine:latest /bin/sh
</pre>