# Frequently Used Commands (FUC)

## Configurations
* Python gitignore file [python.gitignore](config/python.gitignore)
* Python header template [python.header](config/python.header)
* Git configuration file [git.config](config/git.config)

## Copy & Move
```
gcp <source> <destination>   # copy with progress
```

## Compression
```
tar -czvf tar-archive-name.tar.gz <source>     # compress folder to tar.gz
tar -xzvf tar-archive-name.tar.gz              # extract a tar.gz compressed archive
tar -cjvf tar-archive-name.tar.bz2 <source>    # compress folder to tar.bz2
tar -xjvf tar-archive-name.tar.bz2             # extract a tar.bz2 compressed archive
```

## Search
```
grep -rin <text_pattern> .    # searching plain-text in files of current subdirectory that matches pattern
```

## Git
```
git push <remote_name> --delete <branch_name>    # delete a remote GIT branch
git tag -a <tag_name> -m <comment>               # add tag for repository
```
