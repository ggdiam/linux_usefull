##Docker usefull commands

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
