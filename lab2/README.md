# Lab2 Frequently Used Commands

## Table of Contents
- [Running Launch Files and Setting Parameters](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab2#running-launch-files-and-setting-parameters)

## Running Launch Files and Setting Parameters

There are two ways to launch launch files:

If your package is built/sourced correctly, you should not need to include any absolute path in the command; just include "launch_file.launch.xml".

```bash
ros2 launch <package_name> <launch_file>
```

Alternatively, include the full path:

```bash
ros2 launch <path_to_launch_file>
```

To set parameters during launch, use the `--param` argument:

```bash
ros2 launch  <package_name> <launch_file> --param <param_name>:=<value>
```

This will override any parameters set in the launch file and in any yaml file.


## Visualization Markers

In future labs, ROS's visualization tools will become your friend. ROS2 provides the Marker message type to visualize shapes, lines, and other objects in RViz. In this example below, we use a `Marker.LINE_STRIP` type, but many types exist, i.e. `Marker.SPHERE`, `Marker.ARROW`, `Marker.POINTS`, `Marker.TRIANGLE_LIST`. ROS also has `MarkerArray`s for visualizing large numbers of markers.

This simple example demonstrates the function of a `Marker.LINE_STRIP`:

```python
# In your node's constructor, define the publisher:
self.publisher = self.create_publisher(Marker, "/visualization", 1)

# In a callback function, publish the visualization:
line_strip = Marker()
line_strip.type = Marker.LINE_STRIP
line_strip.header.frame_id = frame

# Set size and color
line_strip.scale.x = 0.1
line_strip.scale.y = 0.1
line_strip.color.a = 1.
line_strip.color.r = color[0]
line_strip.color.g = color[1]
line_strip.color.g = color[2]

# Fill line with desired values
for xi, yi in zip(x, y):
    p = Point()
    p.x = xi
    p.y = yi
    line_strip.points.append(p)

# Publish the line
self.publisher.publish(line_strip)
```

