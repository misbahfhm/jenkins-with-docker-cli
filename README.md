# jenkins-with-docker-cli

## Build & Run
```bash
docker build -t jenkins-with-docker .

docker stop jenkins
docker rm jenkins

docker run -d \
  -p 8080:8080 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --name jenkins \
  jenkins-with-docker
```