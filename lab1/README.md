# Lab1 Frequently Used Commands

## Table of Contents
- [Using the Docker Container](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#using-the-docker-container)
    - [Starting Up](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#starting-up)
    - [Shutting Down](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#shutting-down)
- [Intro to Linux](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#intro-to-linux)
    - [SSH](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#ssh)
    - [SCP](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#scp)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Intro to ROS](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#intro-to-ros)

## Using the Docker Container
### Starting Up
```
docker compose up
```
### Shutting Down
```
docker compose down
```
## Intro to Linux
### SSH
```
ssh [username]@[hostname or IP address]
```

For example, to connect to `athena`,
```
ssh [kerberos]@athena.dialup.mit.edu
```
### SCP
#### Copy from local to remote
```
scp [file_name] [remoteuser]@[remotehost]:[/remote/directory]
```

For example, to copy `./test.txt` to remote at `~`,
```
scp ./test.txt [kerberos]@athena.dialup.mit.edu:~
```

#### Copy from remote to local
```
scp [remoteuser]@[remotehost]:[/remote/directory] .
```

## Intro to ROS

Coming soon...
