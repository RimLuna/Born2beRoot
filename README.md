# Debian 11

### sudo
```
rbougssi@rbougssi42:~$ su -
Password: 
root@rbougssi42:~# apt install sudo
root@rbougssi42:~# dpkg -l | grep sudo
ii  sudo                       1.9.5p2-3                      amd64        Provide limited super user privileges to specific users
```
### add user to sudo group
```
root@rbougssi42:~# adduser rbougssi sudo
Adding user `rbougssi' to group `sudo' ...
Adding user rbougssi to group sudo
Done.
root@rbougssi42:~# groups  rbougssi
rbougssi : rbougssi cdrom floppy sudo audio dip video plugdev netdev
```
### SSH port
```
root@rbougssi42:~# apt install net-tools
root@rbougssi42:~# netstat -tulpn
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name    
tcp        0      0 127.0.0.1:39283         0.0.0.0:*               LISTEN      514/node            
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      382/sshd: /usr/sbin 
tcp6       0      0 :::22                   :::*                    LISTEN      382/sshd: /usr/sbin 
udp        0      0 0.0.0.0:68              0.0.0.0:*                           292/dhclient
```
