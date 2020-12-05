# Jenkins-Docker (Docker in Jenkins Docker)

```sh
docker volume create jenkins-data
```

```sh
docker run --name jenkins-docker --restart unless-stopped -it -u root -p 8080:8080 -p 50000:50000 \
-v /var/run/docker.sock:/var/run/docker.sock \
-v jenkins-data:/var/jenkins_home \
pitchanon/jenkins-docker:1.0.0
```
