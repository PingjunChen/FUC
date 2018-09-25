# sftp CheatSheet
### Login to server
```
$ sftp <user_name>@<server_ip>                  # login to default home directory of the server
$ sftp <user_name>@<server_ip>:<remote_dir>     # login into remote directory of the server
```

### File transfer 
```
$ get <server_path> <local_path>                # Download file from server
$ put <local_path> <server_path>                # Upload file to the server
```

### Command
```
$ !<command>                                    # Local command
$ <command>                                     # Remote command
```

### Exit server
```
$ exit/quit/bye                                 # exit from server
```
