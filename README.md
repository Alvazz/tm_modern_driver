#TM Modern Driver
A driver with joint velocity control for Techman Robot TM5.

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
during the execution
* input ```start``` to connect to techman robot
* input ```halt``` to disconnect to techman robot
* input ```quit``` to exit the program

if the connection is success
* input ```datart``` to print all robot_state_rt once
* input ```show``` to print robot_state cyclic, type ```1, 2, ..., 9, 0``` to change data type, type ```q``` to leave the loop
* input ```clear``` to clear terminal.
* ``` movjabs j1 j2 j3 j4 j5 j6``` set absolut joint position (rad)

TODO:
- the usage of all robot commands
- joint velocity control commands
