402 Test
===========

The ROS2 CANopen Stack has a mock slave that enables testing the functionalities
of the 402_driver. In order to launch the test system you need to enable vcan0.

The following command will launch a CIA402 test system for lifecycled service-based operation:

.. code:: bash
  
  ros2 launch canopen_tests cia402_lifecycle_setup.launch.py