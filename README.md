# ROS AMR interoperability packages

This repository hosts a collection of ROS packages to ease
the integration of ROS based robots with different interoperability
standards, with a focus on AMRs (Autonomous Mobile Robots).

## Packages

The following packages are included in this repository:

### Full Control Fleet Adapter for RMF and InOrbit

The [rmf_inorbit_fleet_adapter](https://github.com/inorbit-ai/ros_amr_interop/tree/humble-devel/rmf_inorbit_fleet_adapter) package contains a Full Control [Open-RMF](https://github.com/open-rmf/rmf#robotics-middleware-framework-rmf) Fleet Adapter that allows RMF to control a fleet of autonomous robots through the InOrbit API.
For demonstrations of this adapter or a template to configure your own fleet, visit the the InOrbit RMF [Fleet Adapter Examples](https://github.com/inorbit-ai/rmf_inorbit_examples) repository.

### VDA5050 Connector for ROS2

The [vda5050_connector](https://github.com/inorbit-ai/ros_amr_interop/tree/galactic-devel/vda5050_connector#readme)
package provides a set of ROS2 nodes for connecting a ROS2-based robot to a [VDA5050 Master Control](https://github.com/VDA5050/VDA5050/blob/main/VDA5050_EN.md#-5-process-and-content-of-communication).

If you want to develop a VDA5050 adapter for your robots, please check out our [VDA5050 Adapter Examples repository](https://github.com/inorbit-ai/vda5050_adapter_examples) to get started.

### Mass Robotics AMR Interop Sender for ROS2

The [massrobotics_amr_sender_py](https://github.com/inorbit-ai/ros_amr_interop/tree/foxy-devel/massrobotics_amr_sender_py#readme)
package provides a ROS2 node written in Python that takes input from a
ROS2 system and publishes it to a [Mass Robotics Interop compliant
Receiver](https://github.com/MassRobotics-AMR/AMR_Interop_Standard/tree/main/MassRobotics-AMR-Receiver).

Mapping of different data elements from the ROS2 system into Mass
Robotics Interop messages can be customized through a YAML configuration
file.

## Related Initiatives

The topic of AMR interoperability is in a fluid state of evolution. For this reason, it is worth it to keep track of other standards, initiatives, libraries and efforts related to this topic.

The following is an incomplete and growing list of such related topics:

* [Isaac Mission Dispatch](https://github.com/nvidia-isaac/isaac_mission_dispatch) is NVIDIA's open source cloud micro-services enabling fleet management software to submit missions to multiple robots and monitor the robot and mission states. The communication between Mission Dispatch and robots is designed per VDA5050 protocol and uses MQTT.
* [Open-RMF](https://osrf.github.io/ros2multirobotbook/) (formerly RMF Core) is an open source framework based on ROS 2 to enable the interoperability of heterogeneous fleets of any type of robotics systems.
* [Mass Robotics AMR Interoperability Standard](https://github.com/MassRobotics-AMR/AMR_Interop_Standard) aims to help organizations deploy AMRs from multiple vendors and have them coexist effectively.
* [VDA 5050](https://github.com/VDA5050/VDA5050) AGV Communications Interface describes an interface for communication between driverless transport vehicles (AGV) and a master control system over MQTT using standardized JSON messages.
* [OPC Unified Architecture](https://opcfoundation.org/about/opc-technologies/opc-ua/) (OPC UA) is a machine to machine communication protocol for industrial automation developed by the OPC Foundation
  * [ros_opcua_communication](http://wiki.ros.org/ros_opcua_communication) ROS bindings for different open-source OPC-UA implementations

We expect to keep curating the set of relevant topics with the contribution of the community.

## Development

Install [pre-commit](https://pre-commit.com/) in your computer and then set it up by running `pre-commit install` at the root of the cloned project.

## Build Status

| Service | Foxy  | Galactic |
| :---: | :---: | :---: |
| ROS Build Farm | [![Build Status](http://build.ros2.org/job/Fdev__ros_amr_interop__ubuntu_focal_amd64/badge/icon)](http://build.ros2.org/job/Fdev__ros_amr_interop__ubuntu_focal_amd64/) |  [![Build Status](http://build.ros2.org/job/Gdev__ros_amr_interop__ubuntu_focal_amd64/badge/icon)](http://build.ros2.org/job/Gdev__ros_amr_interop__ubuntu_focal_amd64/) |

| Package | Foxy Source | Foxy Debian | Galactic Source | Galactic Debian |
| :---: | :---: | :---: | :---: | :---: |
| rmf_inorbit_fleet_adapter | N/A | N/A | N/A | N/A |
| vda5050_connector | N/A | N/A | [![Build Status](http://build.ros2.org/job/Gsrc_uF__vda5050_connector__ubuntu_focal__source/badge/icon)](http://build.ros2.org/job/Gsrc_uF__vda5050_connector__ubuntu_focal__source/) | [![Build Status](http://build.ros2.org/job/Gbin_uF64__vda5050_connector__ubuntu_focal_amd64__binary/badge/icon)](http://build.ros2.org/job/Gbin_uF64__vda5050_connector__ubuntu_focal_amd64__binary/) |
| vda5050_msgs | N/A | N/A | [![Build Status](http://build.ros2.org/job/Gsrc_uF__vda5050_msgs__ubuntu_focal__source/badge/icon)](http://build.ros2.org/job/Gsrc_uF__vda5050_msgs__ubuntu_focal__source/) | [![Build Status](http://build.ros2.org/job/Gbin_uF64__vda5050_msgs__ubuntu_focal_amd64__binary/badge/icon)](http://build.ros2.org/job/Gbin_uF64__vda5050_msgs__ubuntu_focal_amd64__binary/) |
| vda5050_serializer | N/A | N/A | [![Build Status](http://build.ros2.org/job/Gsrc_uF__vda5050_serializer__ubuntu_focal__source/badge/icon)](http://build.ros2.org/job/Gsrc_uF__vda5050_serializer__ubuntu_focal__source/) | [![Build Status](http://build.ros2.org/job/Gbin_uF64__vda5050_serializer__ubuntu_focal_amd64__binary/badge/icon)](http://build.ros2.org/job/Gbin_uF64__vda5050_serializer__ubuntu_focal_amd64__binary/) |
| massrobotics_amr_sender | [![Build Status](http://build.ros2.org/job/Fsrc_uF__massrobotics_amr_sender__ubuntu_focal__source/badge/icon)](http://build.ros2.org/job/Fsrc_uF__massrobotics_amr_sender__ubuntu_focal__source/) | [![Build Status](http://build.ros2.org/job/Fbin_uF64__massrobotics_amr_sender__ubuntu_focal_amd64__binary/badge/icon)](http://build.ros2.org/job/Fbin_uF64__massrobotics_amr_sender__ubuntu_focal_amd64__binary/) | [![Build Status](http://build.ros2.org/job/Gsrc_uF__massrobotics_amr_sender__ubuntu_focal__source/badge/icon)](http://build.ros2.org/job/Gsrc_uF__massrobotics_amr_sender__ubuntu_focal__source/) | [![Build Status](http://build.ros2.org/job/Gbin_uF64__massrobotics_amr_sender__ubuntu_focal_amd64__binary/badge/icon)](http://build.ros2.org/job/Gbin_uF64__massrobotics_amr_sender__ubuntu_focal_amd64__binary/) |
