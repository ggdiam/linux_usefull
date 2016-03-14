##Docker usefull commands

**bash with no container**
```
docker run --rm -it training/webapp /bin/bash
```

**see image**
```
docker inspect training/webapp
```

**mount folder /Users/alex/docker to image folder /home***
```
docker run --rm -it -v /Users/alex/docker:/home ubuntu /bin/bash
```

**run image with 80 port listen**
```
docker run --rm -it -p 80:8080 image-name
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
