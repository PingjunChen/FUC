fstab
========
The configuration file "/etc/fstab" contains the necessary information to
automate the process of mounting partitions.

Mount partitions
--------

Add following line to the end of **fstab** file.

:code:`<partition> <mount_point> auto auto,user,rw 0 0`

Following are two examples:

:code:`/dev/sdb1 /data/.data1 auto auto,user,rw 0 0`

:code:`/dev/sdc1 /data/.data2 auto auto,user,rw 0 0`

Join partitions
--------

`mhddfs <https://romanrm.net/mhddfs>`_: tool for joining several filesystems
together to form a single larger one.

Install mhddfs

:code:`$ sudo apt-get install mhddfs`

Create folder for merging

:code:`mkdir /data/main`

Add the following line to the end of fstab

:code:`mhddfs#/data/.data1,/data/.data2 /data/main fuse defaults,allow_other 0 0`
