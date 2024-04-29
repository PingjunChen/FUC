git command
========

Show difference
--------

On modified file

:code:`$ git diff <file_path>`

On staged file

:code:`$ git diff --staged <file_path>`


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


Remote
--------

Set up upstream remote

:code:`git remote add upstream https://github.com/repo`

Update local repo

:code:`git pull upstream <branch_name>`

Push to upstream

:code:`git push upstream <branch_name>`
