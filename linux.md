How to know filesystem of disk:
-------------------------------
fsck -N /dev/sda

How to know mapping between disk and partitions:
------------------------------------------------
lsblk

another usefull tools: http://www.binarytides.com/linux-command-check-disk-partitions/


Operation about logical group and lvm:
--------------------------------------
vgdisplay

vgscan

create lvm http://www.thegeekstuff.com/2010/08/how-to-create-lvm


Formating partition:
--------------------
mkfs.ext4 /dev/sdb1


Release memory:
---------------
http://wiki.tuxunix.com/index.php/Liberer_de_la_m%C3%A9moire_sous_Linux


Kernel messages:
----------------
dmesg --reltime


Tcpdump:
--------
https://openmaniak.com/fr/tcpdump.php

tcpdump  -A -i  eno16777984  -w /tmp/output


Open port:
----------
lsof -i -P | grep -i "listen"

lsof -i  -P -n

Rpm commands:
-------------
List files in rpm: rpm -ql collectd

List rpm: rpm -qa

List repo: yum repolist


Threads number for a pid:
-------------------------
ps -o nlwp 13291


Ssh tunnel:
-----------
ssh -N -L localhost:4242:bc1:4242 rniveau@x.x.x.x


Java cli:
---------
Memory dump: jmap -dump:format=b,file=cheap.bin 60391

Thread dump: jstack 10794 > /tmp/thread-start.tdump

Classloader dump: jmap -clstats 5425