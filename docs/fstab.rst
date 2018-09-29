fstab
========
The configuration file "/etc/fstab" contains the necessary information to
automate the process of mounting partitions

Mount partitions
--------

Add following line to the end of **fstab** file.

:code:`<partition> <mount_point> auto auto,user,rw 0 0`

Following are two examples
:code:`/dev/sdc1 /data/.data1 auto auto,user,rw 0 0`

:code:`/dev/sdd1 /data/.data2 auto auto,user,rw 0 0`

Join partitions
--------

`mhddfs <https://romanrm.net/mhddfs>`_: join several filesystems together to
form a single larger one.

Install mhddfs

:code:`$ sudo apt-get install mhddfs`

Join multiple partitions

:code:`mhddfs#/data/.data1,/data/.data2 /data/main fuse defaults,allow_other 0 0`
