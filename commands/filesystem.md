# Filesystem

## File number
```
$ ls -ls *.<ext> | wc -l                     # Number of files is less
$ find -type f -name '*.<ext>'  | wc -l      # More than 100, 000 files
```

## Storage usage
```
du -hs *                                   # check the size of all subdirectories
du -hs <directory name>                    # check the szie of a certain directory
df -h                                      # check the usage of file system
```
