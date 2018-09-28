# User Management

```
adduser <username>               # add user with full profile and info (always recommended)
useradd <username>               # add user with his name only (low level utility, prefer not to use)
usermod -aG sudo <username>      # add user to sudo group
compgen -u                       # list all user names
userdel -r <username>            # delete user's home directory and mail spool
```
