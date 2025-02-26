# Lab2 Frequently Used Commands

## Table of Contents
- [Running Launch Files and Setting Parameters](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab2#running-launch-files-and-setting-parameters)
    - [Starting Up](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#starting-up)
    - [Shutting Down](https://github.com/mit-rss/frequently_used_instructions/tree/main/lab1#shutting-down)

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
