# Compression

## Tar and untar
```
$ tar -cvf tar-archive-name.tar <source>          # Create tar archive File
$ tar -xvf tar-archive-name.tar                   # Untar files in current directory
$ tar -xvf tar-archive-name.tar -C <destination>  # Untar files to a specific directory
$ tar -tvf tar-archive-name.tar                   # List content of tar archive file
```

## Compress and uncompress
```
$ tar -czvf tar-archive-name.tar.gz <source>     # Compress folder to tar.gz
$ tar -xzvf tar-archive-name.tar.gz              # Extract a tar.gz compressed archive
$ tar -cjvf tar-archive-name.tar.bz2 <source>    # Compress folder to tar.bz2
$ tar -xjvf tar-archive-name.tar.bz2             # Extract a tar.bz2 compressed archive
```
