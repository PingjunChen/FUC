mount ntfs disk to mac
========

Find device information
--------

:code:`$ diskutil info /Volumes/YOUR_NTFS_DISK_NAME`

Eject the disk
--------

Create with specific python version

:code:`$ hdiutil eject /Volumes/YOUR_NTFS_DISK_NAME`

Make a new folder which to be mounted
--------

:code:`$ sudo mkdir /Volumes/MYHD`

MOunt the disk to mac
--------

:code:`$ sudo mount_ntfs -o rw,nobrowse /dev/disk2s2 /Volumes/MYHD/`
