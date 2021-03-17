#  Question
Tag and push the docker image that you built to DockerHub. Don't forget to docker login first ;)

###  Answer:
First we pull ubuntu image and run it and execute in it and make test-directory in it then commit,login and push it.
<pre>
docker pull ubuntu
docker run -it -d ubuntu
docker exec -it ubuntucontainerID bash
mkdir test-directory
</pre>
then commit this and tag this
<pre>
	docker commit containerid username/myimage:1.0 
</pre>
Enter Docker Hub credentials
<pre>
docker login
</pre>
finally push your image to docker hub
<pre>
docker push username/myimage:1.0 
	</pre>