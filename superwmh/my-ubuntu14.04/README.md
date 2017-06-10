## docker build

```
docker build -t my14.04 ./
```

## docker run

```
$ docker run -it --rm -p 8081:80 -v /data:/data my14.04 /bin/bash
```

or

```
$ docker run -it --rm -p 8081:80 -v /data:/data my14.04 /data/docker/bin/run-my-service.sh
```

* /data/docker/bin/run-my-service.sh

```
#!/bin/bash
ln -s /data/docker/conf/cms-portal-docker.conf /etc/apache2/sites-enabled/
/etc/init.d/apache2 start
/bin/bash
```
