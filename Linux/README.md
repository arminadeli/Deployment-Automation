1-1
sudo su
ls -l /etc/shadow
chown root:root /etc/shadow
chmod 600 /etc/shadow
1-2
ls -l /etc/gshadow
chown root:root /etc/gshadow
chmod 600 /etc/gshadow

1-3
ls -l /etc/group

1-4
ls -l /etc/passwd
chmod 644 /etc/passwd

2-1
adduser sam
adduser joe
adduser amy
adduser sara
adduser admin

2-2
usermod -g root admin

3-1 usermod -g root admin
3-2
 usermod -g engineers sam
 usermod -g engineers joe
 usermod -g engineers amy
 usermod -g engineers sara
3-3
 usermod -g engineers sam
3-4
chown root:engineers engineers

4-1
apt install lynis
4-2
man lynis
4-3
lynis audit system

Bouns
1- apt install chkrootkit
2- man chkrootkit
3- chkrootkit -x
