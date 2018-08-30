## Login Server without Password
### 1. Generate authentication keys in local machine
```
ssh-keygen -t rsa
```
### 2. Create ~/.ssh directory in server if not exist
```
mkdir -p .ssh
```
### 3. Append public key in local machine to server 
```
cat .ssh/id_rsa.pub | ssh server_username@server_ip 'cat >> .ssh/authorized_keys'
```
### 4. Login 
```
ssh server_username@server_ip
```
