Lifecycle Operation
===================

During lifecycled operation, the CANopen stack can be controlled using
ROS2's lifecycle feature. All master and driver nodes are lifecycled and a lifecycle
manager is used to manage the lifecycle of the spawned master and driver nodes.
The lifecycled operation has the advantage, that all nodes of the running
stack except the lifecycle_device_container can be controlled and reset using
the ROS2 lifecycle feature.

Operation
----------------
When using the lifecycled mode, the user launches the LifecycleDeviceContainerNode
and passes the bus configuration file. Once launched, the LifecycleDeviceContainerNode
will start loading the MasterNode, DriverNodes and DeviceManager components. Once all
nodes were successfully loaded, the user has the possibility to control all devices using
the LifecycleDeviceManagerNode's lifecycle.
The user can first configure the LifecycleDeviceManagerNode, which will the load all
necessary information from parameters and configuration files.
When activates the LifecycleDeviceManagerNode, the node will first configure and activate
the MasterNode. Once the MasterNode was successfully brought to active state, the
LifecycleDeviceManagerNode will configure and activate the DriverNodes.

.. uml:: startup.puml
