Overview
========
ros2_canopen provides nodes for interfacing with CANopen devices. The library builds upon the professional and open source
lelycore canopen library as opposed to the previous ros_canopen stack.
In ros2_canopen the bus configuration is simplified through the use of
lelycore's configutaration toolchain.

ros2_canopen contains a number of packages that serve different serve different puposes.

* **canopen**:
  
  Meta-package for easy installation and contains overall documentation
  of the ros2_canopen stack.

* **lely_core_libraries**:
  
  A colcon package wrapper for the lelycore canopen library, for convenient
  installation with rosdep.

* **canopen_interfaces**:
  
  The ros2 interface definitions for non standard messages and services used by ros2_canopen.

* **canopen_core**:
  
  Contains the core structures of the ros2_canopen stack such as the device manager
  and the master node and the driver node interface.

* **canopen_base_driver**:
  
  This package contains the base implementation of a ROS2 CANopen device driver. It can base
  used by other drivers for easy extension.

* **canopen_proxy_driver**:
  
  Contains an implmentation of a proxy driver which simply forwards CANopen functionality
  for a specific device via ROS2 services and messages.

* **canopen_402_driver**:

  Contains an implementation of the CIA402 profile for motion controllers and exposes
  the profiles functionalities via ROS2 services and messages. The implementation is
  copied from ros_canopen/canopen_402 and this package is licensed accordingly under 
  GNU Lesser General Public License v3.0!

* **canopen_utils**: 
  
  Contains utilities to simplifiy testing and interaction with CANopen devices.

* **canopen_mock_slave**:
  
  Contains CANopen slaves that for testing purposes. Currently, this includes a slave
  for testing simple CANopen interaction and a slave that implements CIA402 profile
  partially.

* **canopen_tests**:
  
  This package contains launch_tests for testing ros2_canopen against mock slaves.
  

