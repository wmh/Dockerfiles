## docker build

```
docker build -t myphp7 ./
```

## docker run

```
docker run -d -p 8080:80 \
  -v /data:/data \
  myphp7
```

## docker run with mysql

```
docker run --name mysql57 -e MYSQL_ROOT_PASSWORD=mysql-pw-123 -d mysql:5.7
```

```
docker run -d -p 8080:80 \
  --link mysql57:mysql \
  -v /data:/data \
  myphp7
```
