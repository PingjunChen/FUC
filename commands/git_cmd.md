# Git

## Delete branch
```
$ git branch -D <branch_name>                      # Delete local branch
$ git push <remote_name> --delete <branch_name>    # Delete a remote branch
```

## Tag
```
$ git tag -a <tag_name> -m <comment>               # Add tag for repository
$ git tag -l                                       # List all tag
$ git tag -d <tag_name>                            # Delete local tag
$ git push --delete origin <tag_name>              # Delete remote tag
```
