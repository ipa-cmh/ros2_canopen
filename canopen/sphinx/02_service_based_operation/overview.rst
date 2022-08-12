Overview
========

This section describes, how the ROS2 CANopen stack can be used with a service
based interface. This should only be done for applications without fast control loops
running via the stack. Two modes of operation are possible.

* **Lifecycled Operation**
  
  When using this operation mode, the stack leverages ROS2's node lifecycle features to
  make the ROS2 CANopen stack more resilient.

* **Legacy Operation**
  
  When using the legacy operation mode, the stack will use plain ROS2 nodes. This has disadvantages
  when it comes to runtime recovery.