sshfs
========
`sshfs <https://github.com/libfuse/sshfs>`_ is network filesystem client to
connect to other macines, which allows server to use code and data from local
machine with no need for copying.

Installation
--------
:code:`$ sudo apt-get install sshfs`

Create connection
--------
In server machine, link server directory to local directory. Note to avoid using
soft link for both local and server directory.

:code:`$ sshfs -o nonempty <username>@<local_ip>:local_dir server_dir`

List sshfs mounting points
--------
:code:`$ ps -elf | grep sshfs`

Unmount the connection
--------
:code:`$ sudo umount server_dir`

If sudden problems happen, use fusermount instead:
--------
:code:`$ fusermount -u server_dir`



