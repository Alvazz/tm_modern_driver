# TM Modern Driver
A driver with new joint velocity control for Techman Robot TM5.

## Installation
```
mkdir build
cd build
cmake ..
make
```

## Usage
To start this test program:
```
$ ./test_tm_driver 192.168.0.10
```
**Connection command**
* input ```start``` to connect to techman robot
* input ```halt``` to disconnect to techman robot
* input ```quit``` to exit the program

**if the connection is success**
* input ```datart``` to print all robot_state_rt once
* input ```show``` to print robot_state cyclic, type ```1, 2, ..., 9, 0``` to change data type, type ```q``` to leave the loop
* input ```clear``` to clear terminal.
* input ```emstop``` to stop immediately. **(NOTE: this command need ```run``` to restart robot)**

## Motion API

### Absolute Joint position
- The input joint position argument is **radius**
```
movjabs j1 j2 j3 j4 j5 j6
```

### Reference Joint position
- The input joint position argument is **radius**
- This command will set joint psition based on last position.
```
movjrel j1 j2 j3 j4 j5 j6
```



### Absolute TCP Cartesian position
- The input cartesian position argument is **meter**
```
movlabs x y z a b c
```
### Joint velocity Control
- Turn on joint velocity control mode : ```jointspdon```
- Turn off joint velocity control mode : ```jointspdoff```
- Set joint velocity, the input argument is in **rad/s**
```
movjspd v1 v2 v3 v4 v5 v6
```
**NOTE : Joint velocity mode need to turn on before using the command and by turning off to use other motion API**


## TODO:
- the usage of all robot commands
- integrate into ROS indigo package
