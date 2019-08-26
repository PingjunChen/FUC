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

REmove big file if commited wrongly

:code:`$ git filter-branch --tree-filter 'rm -rf path/to/your/file' HEAD`
:code:`$ git push`
