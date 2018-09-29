compression
========

Tar and untar
--------

Create tar archive File

:code:`$ tar -cvf tar-archive-name.tar <source>`

Untar files in current directory

:code:`$ tar -xvf tar-archive-name.tar`

Untar files to a specific directory

:code:`$ tar -xvf tar-archive-name.tar -C <destination>`

List content of tar archive file

:code:`$ tar -tvf tar-archive-name.tar`


Compress and uncompress
--------

Compress folder to tar.gz

:code:`$ tar -czvf tar-archive-name.tar.gz <source>`

Extract a tar.gz compressed archive

:code:`$ tar -xzvf tar-archive-name.tar.gz`

Compress folder to tar.bz2

:code:`$ tar -cjvf tar-archive-name.tar.bz2 <source>`

Extract a tar.bz2 compressed archive

:code:`$ tar -xjvf tar-archive-name.tar.bz2`
