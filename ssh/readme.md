### Generate ssh keys
```console
$ ssh-keygen -t rsa
```

### Add Public SSH Key to Remote Server in a Single Command
```console
$ cat ~/.ssh/id_rsa.pub | ssh user@hostname 'cat >> .ssh/authorized_keys'
```
