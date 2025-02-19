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
    - [Managing Packages](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#managing-packages)
    - [ROS Debugging Commands](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#ros-debugging-commands)

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

### Managing Packages

#### Creating a ROS Package
```
ros2 pkg create --build-type ament_python <package-name>
```

#### Colcon Build
Always build in ```~/racecar_ws```! 

```--symlink-install``` allows you to edit code in nodes without building after each change
```
colcon build --symlink-install
```

```--packages-select``` allows you to select a specific package to build 
```
colcon build --packages-select <package_name> --symlink-install
```

#### Sourcing Code
Make sure to source in every terminal
```
source install/setup.bash
```

### ROS Debugging Commands

Displaying rqt_graph (run in GUI only)
```
rqt_graph
```

View tf-tree (run in GUI only)
```
ros2 run rqt_tf_tree rqt_tf_tree
```

List all packages 
```
ros2 pkg list
```

List all active topics
```
ros2 topic list
```

Monitor output of topic
```
ros2 topic echo <topic_name>
```

List all active nodes
```
ros2 node list
```

Monitors the frequency of messages published on a topic
```
ros2 topic hz <topic_name>
```

Display message type of a topic
```
ros2 topic type <topic_name>
```

