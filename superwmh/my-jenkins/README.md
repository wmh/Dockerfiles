## docker build

```
docker build -t myjenkins ./
```

## docker run

```
docker run \
  -u root \
  --restart unless-stopped \
  -d \
  -p 8070:8080 \
  -p 50000:50000 \
  -v jenkins-data:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  myjenkins
```
