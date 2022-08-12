Usage Considerations
====================

Before making decisions about and starting the implementation of your CANopen-based application, you should make sure,
you understand the requirements of your application. The ROS2 CANopen stack offers 2 operation modes. One is operation
via plain ROS2 services and the other is operation via ROS2 control.

The service-based operation is recommended for lower frequency control loops only.
