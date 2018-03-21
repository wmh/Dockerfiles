## docker build

```
docker build -t myphp71 ./
```

## docker run

```
docker run -d \
  -u root \
  -p 8080:80 \
  -v /data:/data \
  myphp71
```

## docker-compose with mysql

```
docker-compose up -d
```

## docker run with mysql

```
docker run --name mysql57 -e MYSQL_ROOT_PASSWORD=mysql-pw-123 -d mysql:5.7
```

```
docker run -d \
  --link mysql57:mysql \
  -u root \
  -p 8080:80 \
  -v /data:/data \
  myphp71
```
