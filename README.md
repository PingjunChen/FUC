# Frequently Used Commands (FUC)

## CheatSheets
* [ZappyCode's Django 2 cheatsheet](cheatsheets/django/Django2-Cheat-Sheet.pdf)
* [Virtualenv cheatsheet](cheatsheets/virtualEnvCheatsheet.md)
* [CondaEnv cheatsheet](cheatsheets/condaEnvCheatsheet.md)
* [Pandoc cheatsheet](cheatsheets/pandocCheatsheet.md)
* [Docker cheatsheet](cheatsheets/dockerCheatsheet.md)
* [tmux cheatsheet](cheatsheets/tmuxCheatsheet.md)
* [sftp cheatsheet](cheatsheets/sftpCheatsheet.md)

## Commands
* [Compression](commands/compression.md)
* [UserManagement](commands/user.md)
* [Filesystem](commands/filesystem.md)
* [Apache](commands/apache.md)
* [GitCmd](commands/git_cmd.md)

## Configurations
* [Python gitignore file](config/python.gitignore)
* [Python header template](config/python.header)
* [Git configuration file](config/git.config)
* [SSH login server without password](config/ssh_login_no_passwd.md)
* [.bashrc configuration](config/bashrc.config)
* [fstab configuration](config/fstab.config)


## Process
* kill process with certain conditions
```
ps -ef | grep <command> | awk '{print $2}' | xargs kill -9  
```
