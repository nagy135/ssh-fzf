# ssh-fzf
Simple script that lets you quickly connect to servers via ssh

# Key features
Supports:
* multiple servers (meaning name => ip address)
* multiple users (if specified, gives you selector to choose user)

Also:
* can paste `user@ip_address` into your clipboard
* perform dialog to scp from/to server (copy files)

# Dependencies
* [fzf](https://github.com/junegunn/fzf)
* bash
* ssh

# Install
Simply clone repository and put both `ssh-fzf` as well as `connections` to folder within `$PATH` or add this repository to `$PATH` variable

# Usage
Run script and optionally pass argument
* `clip`: to just copy connection to string (to paste to some other tool)
* `scp`: to get to guided copy from/to server via few dialogs

# Configuration
Configured using bash array where **key** is server name and **value** is actual connection.
If you connect using multiple users, separate them by semicolon like in example bellow.
```
conn_pairs["my_server"]="user@127.0.0.1"
conn_pairs["my_server_multiple_users"]="user@127.0.0.1;resu@127.0.0.1"
```

# TODO
* Wayland version
* AUR package
