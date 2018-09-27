sftp
=================
SSH File Transfer Protocol, a network protocol used for secure file transfer over secure shell.

Login to server
-----------------
Login to user home directory of the server.

:code:`$ sftp <user_name>@<server_ip>`

Login to specific directory of the server.

:code:`sftp <user_name>@<server_ip>:<remote_dir>`

File transfer
-----------------
Download file to local machine.

:code:`$ get <server_path> <local_path>`

Upload local file to server.

:code:`$ get <local_path> <server_path>`

Command
-----------------
Command for local host.

:code:`$ !<command>`

Command for server.

:code:`$ <command>`

Exit server
-----------------
exit from server to local machine.
:code:`$ bye`
