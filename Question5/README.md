# Question

Writing your first docker compose file
Before to deep dive in the orchestators tools, we are going to start here with the most basic, yes docker-compose , you will need to do the following.
1)Create a dockerfile that will have python installed on it (from python base image),  and install the flask framework. <br/>
2)Create an redis image (from redis base image) that will serve as the database of the python app.<br/>

3)Create an nginx dockerfile (from nginx base image)  that will work as your proxy server.<br/>

With all of this setup, what you need to do is the following.
The application logic, can be whatever you like, make it simple :)
These are few requirements. 
<br/>
The python app will need to talk with the redis database. <br/>
All of this configuration, needs to be automated with docker-compose files.

##### Answer:


Save all these file and configurations
then run these instuction:

#####Command Instructions:
`docker-compose up -d`
<br/>
then open browser:<br/>
enter URL:<br/>
<pre>
http://localhost:8080
</pre>
 
