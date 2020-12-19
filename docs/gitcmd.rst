git command
========

Delete branch
--------

Delete local branch

:code:`$ git branch -D <branch_name>`

Delete remote branch

:code:`$ git push <remote_name> --delete <branch_name>`

Tag
--------

Add tag to current submit

:code:`$ git tag -a <tag_name> -m <comment>`

List all tags

:code:`$ git tag -l`

Delete local tag

:code:`$ git tag -d <tag_name>`

Delete remote tag

:code:`$ git push --delete origin <tag_name>`


Credential
--------

Store credentials

:code:`$ git config --global credential.helper store`


Remote
--------

Set up upstream remote

:code:`git remote add upstream https://github.com/repo`

Update local repo

:code:`git pull upstream master`

Push to upstream

:code:`git push upstream main`
