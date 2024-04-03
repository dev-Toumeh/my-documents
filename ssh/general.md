## add ssh key to Server

### Copy the Public Key to the server
- ssh-copy-id -i ~/.ssh/your_public_key.pub user@host

### Edit the SSH daemon configuration file:
PubkeyAuthentication yes
PasswordAuthentication no

### Restart the SSH service to apply the changes:
- sudo systemctl restart ssh


## make connection Easier (add the following Template to ./ssh/config)

Host raspberrypi
  HostName raspberrypi.local
  User pi
  IdentityFile ~/.ssh/your_private_key


## copy files from local to remote using ssh

    scp local/file/path user@host:/remote/file/path

