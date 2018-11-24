**Docker repo with auth
```
mkdir auth
```

```
docker run --entrypoint htpasswd registry:latest -Bbn myuser mypassword > auth/htpasswd
```

```
docker run -d -p 5000:5000 \
--restart=always \
--name=registry \
-v /data/registry:/var/lib/registry \
-v `pwd`/auth:/auth \
-e "REGISTRY_HTTP_ADDR=0.0.0.0:5000" \
-e "REGISTRY_AUTH=htpasswd" \
-e "REGISTRY_AUTH_HTPASSWD_REALM=Registry Realm" \
-e "REGISTRY_AUTH_HTPASSWD_PATH=/auth/htpasswd" \
registry:latest
```

**Docker auto start containers
```
docker run -dit --restart always  --name mongo -p 27017:27017 -v /data/db:/data/db mvertes/alpine-mongo
docker run -d -p 5000:5000 -v /data/registry:/var/lib/registry --restart always --name registry registry:latest
```

**Docker usefull commands

**bash with no container**
```
docker run --rm -ti training/webapp /bin/bash
```

**see image**
```
docker inspect training/webapp
```

**mount folder /Users/alex/docker to image folder /home***
```
docker run --rm -ti -v /Users/alex/docker:/home ubuntu /bin/bash
```

**run image with 80 port listen**
```
docker run --rm -ti -p 80:8080 image-name
```

**docker-machine ip**
```
docker-machine ip
```

**save image to file**
```
docker save -o <save image to path> <image name>
```
**load image from file**
```
docker load -i <path to image tar file>
```

**see remote images**
```
http://[local_repo]/v2/_catalog
```

**see remote image tags**
```
http://[local_repo]/v2/[image_name]/tags/list
```
