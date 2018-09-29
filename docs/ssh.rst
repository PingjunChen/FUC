ssh
========

Login to server without password
--------

Step 1. Generate authentication keys in local machine.

:code:`$ ssh-keygen -t rsa`

Step 2. Create ~/.ssh directory in server if not exist.

:code:`$ mkdir -p .ssh`

Step 3. Append public key in local machine to server.

:code:`$ cat .ssh/id_rsa.pub | ssh <username>@<server_ip> 'cat >> .ssh/authorized_keys'`

Step 4. Login to server.

:code:`$ ssh <username>@<server_ip>`
