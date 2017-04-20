## Linux usefull commands

**make rsa key**
```ssh-keygen -t rsa```

**copy ssh pub**
```cat ~/.ssh/id_rsa.pub | ssh user@host "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"```

**set bash at login**
```sudo usermod -s /bin/bash username```

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

**root sudoers edit**
```
visudo
```

**show users**
```
cut -d: -f1 /etc/passwd
```
**show groups**
```
cut -d: -f1 /etc/group
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

**determine shell type**
```
echo $0
```
```
ps  -ef | grep $$ | grep -v grep
```

**path to shell**
```
echo $SHELL
```

**utility installed**
```
whereis bash
```
```
which bash
```
