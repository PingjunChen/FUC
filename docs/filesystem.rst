filesystem
========

Get number of all files
--------
When number of file is small, less than 10, 000

:code:`$ ls -ls *.<ext> | wc -l`

When more than 10, 000 files

:code:`$ find -type f -name '*.<ext>'  | wc -l`


Storage usage
--------

Check disk partition usage

:code:`$ df -h`

Check the size of a directory

:code:`$ du -hs <directory>`

Check size of all subdirectories
--------

:code:`$ du -hs *`
