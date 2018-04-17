### ssh tunnel
`ssh -D 8123 -f -C -q -N sammy@example.com`

**Explanation of arguments**

-D: Tells SSH that we want a SOCKS tunnel on the specified port number (you can choose a number between 1025-65536)\
-f: Forks the process to the background\
-C: Compresses the data before sending it\
-q: Uses quiet mode\
-N: Tells SSH that no command will be sent once the tunnel is up
