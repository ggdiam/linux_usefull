## Linux usefull commands

**restart bash:**
```. ~/.bashrc```

**Verify that you have curl installed:**
```which curl```


**linux dist:**
```uname -a```

**free mem:**
```free -h```

**root user**
```
sudo -u root zsh
```
```
whoami
```

**user add / del / set password:**
```
useradd -m user.name
```
```
userdel user.name
```
```
passwd user.name
```

**add user to group:**
```
grep developers /etc/group
```
```
sudo adduser user.name root
```

**change owner**
```chown alex myfile.txt```

**change group**
```chgrp alex myfile.txt```

**show user groups:**
```groups user.name```

