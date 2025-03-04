# Frequently Used Instructions: Lab 4
## Table of Contents
- [Launching the Camera]()
    - [Camera Topic]()
    - [Camera Topic]()
    - [Camera Image Message]()
    - [rqt Image]()
  
- [Launch Files]()
    - [Simulator]()
    - [Racecar]()
  

## Launching the Camera
### Starting Up
```

```
### Shutting Down
```

```
### Camera Topic
```
/zed/zed_node/rgb/image_rect_color
```
### Camera Image Message 
```
ros2 interface show sensor_msgs/msg/Image
```

### Rqt image view
```
rqt image view
```


## Racecar Launch Files 
### Simulator 

Launch Simulator
```
ros2 launch racecar_simulator simulate.launch.xml
```

Parking Sim Launch Command
```
ros2 launch visual_servoing parking_sim.launch.xml
```
### On Racecar

Cone Parking Launch Command
```
ros2 launch visual_servoing parking_deploy.launch.xml
```







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

