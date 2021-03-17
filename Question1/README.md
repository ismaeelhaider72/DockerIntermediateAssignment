#  Question

Create a dockerfile from alpine base image and install and configure awscli. The proposal for this container is to run awscli commands, after that it should die. You must provide the awscli command via entrypoint.

###  Answer:


Dockerfile
<pre>
	FROM alpine:3.11

ENV AWSCLI_VERSION "1.14.10"

RUN apk add --update \
    python \
    py-pip \
    && pip install awscli==$AWSCLI_VERSION --user 
 


ENTRYPOINT ["/root/.local/bin/aws"]
	</pre>

#### Commands instruction

<pre>
docker build  -t awscli-alpine .

docker run -ti awscli-alpine --version
</pre>