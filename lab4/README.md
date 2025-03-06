# Frequently Used Instructions: Lab 4
## Table of Contents
- [Launching the Camera](https://github.com/mit-rss/frequently_used_instructions/blob/main/lab4/README.md#launching-the-camera)
    - [Starting Up](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#starting-up)
    - [Camera Topic](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#camera-topic)
    - [Camera Image Message](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#camera-image-message)
- [Viewing Camera Feed](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#viewing-camera-feed)
- [Racecar Launch Files](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#racecar-launch-files)
    - [Simulator](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#simulator)
    - [Racecar](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab4#on-racecar)
  

## Launching the Camera
### Starting Up
```
#on the car

./run_rostorch.sh

#in another terminal

connect

unset DISPLAY 

#For silver cameras use 'zed', for black cameras use 'zed2'

#for ZED:
ros2 launch zed_wrapper zed_camera.launch.py camera_model:=zed

#for ZED2:
ros2 launch zed_wrapper zed_camera.launch.py camera_model:=zed2
```

### Camera Topic
```
/zed/zed_node/rgb/image_rect_color
```
### Camera Image Message 
```
ros2 interface show sensor_msgs/msg/Image
```

## Viewing Camera Feed
### Through Rviz
1. Open rviz
2. At the bottom left, click add
3. On the pop-up, click to the add by topic tab
4. Scroll down to camera topics and select the Image 

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








