# Frequently Used Commands (FUC)

## Configurations
* [Python gitignore file](config/python.gitignore)
* [Python header template](config/python.header)
* [Git configuration file](config/git.config)
* [SSH login server without password](config/ssh_login_no_passwd.md)
* [.bashrc configuration](config/bashrc.config)
* [fstab configuration](config/fstab.config)

## Cheat Sheets
* [ZappyCode's Django 2 cheatsheet](cheatsheets/django/Django2-Cheat-Sheet.pdf)
* [Virtualenv cheatsheet](cheatsheets/VirtualenvCheatSheet.md)
* [Conda Env cheatsheet](cheatsheets/CondaEnvCheatSheet.md)
* [Pandoc cheatsheet](cheatsheets/PandocCheatSheet.md)

## Copy & Move
```
gcp <source> <destination>   # copy with progression bar
```

## Compression
```
tar -czvf tar-archive-name.tar.gz <source>     # compress folder to tar.gz
tar -xzvf tar-archive-name.tar.gz              # extract a tar.gz compressed archive
tar -cjvf tar-archive-name.tar.bz2 <source>    # compress folder to tar.bz2
tar -xjvf tar-archive-name.tar.bz2             # extract a tar.bz2 compressed archive
```

## User Management
```
adduser <username>               # add user with full profile and info (always recommended)
useradd <username>               # add user with his name only (low level utility, prefer not to use)
usermod -aG sudo <username>      # add user to sudo group
compgen -u                       # list all user names
userdel -r <username>            # delete user's home directory and mail spool 
```

## Filesystem
```
ls -ls *.<ext> | wc -l                     # Number of files is less
find -type f -name '*.<ext>'  | wc -l      # More than 100, 000 files
du -hs *                                   # check the size of all subdirectories
du -hs <directory name>                    # check the szie of a certain directory
df -h                                      # check the usage of file system
```

## Process
```
ps -ef | grep <username> | grep <command> | awk '{print $2}' | xargs kill -9  # kill process with certain conditions 
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

## Docker
```
docker ps                                       # list all existing containers
docker exec -it <container name> /bin/bash      # enter into container
```

## Apache
```
sudo service apache2 restart                 # Restart Apache
tail -n 20 /var/log/apache2/error.log        # Check errorlog
```
