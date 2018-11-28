# docker-jenkins

Here we will upload a dockerized image of jenkins on to Dockerhub.

We have our Dockerfile, which contains the instructions for the machine to create a docker image for jenkins.

The init.groovy file will create a user for our jenkins instance.

The plugins.txt will install the specified plugins for us, so that we do not have to install them on login like we usually do.

Usage Instructions:

First we must build the image. To do this, run:

```bash
docker run -d -p 8080:8080 ilyashusain/jenkins:latest
```

Then we must upload the docker image on to Dockerhub, to do this execute:

```bash
docker tag ilyashusain/jenkins localhost:8080/jenkins
```

since we are localhost, and want to connect on port 8080.

Finally, push to Dockerhub:

```bash
docker push ilyashusain/jenkins
```
