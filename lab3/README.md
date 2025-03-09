If getting `git` permission denied errors (change ownership of the `.git` directory to user instead of root):

```
  sudo chown -R $USER:$USER .git
```

Debugging step with the VESC. If you do

```
ls /dev/ttyACM0
```

and the device is detected, then the VESC is detected and something else might be wrong. If this file doesn't exist, then no VESC is detected and you should try things like recharging the motor battery, trying a different USB port, etc.
