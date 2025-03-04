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








