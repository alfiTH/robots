# Kinova Gen3 7-DOF

The Kinova Gen3 7-DOF is a high-performance robotic arm featuring seven degrees of freedom and ROBOTIQ 85mm parallel gripper, designed for precise manipulation and seamless integration with mobile platforms.

<img src="https://www.kinovarobotics.com/uploads/_1000x1000_crop_center-center_none/22037/Gen3-robot-img-Cover-img-is-loaded-block-1B.webp" alt="P3Bot" width="400"/>

<details>
<summary><strong>Table of Contents</strong></summary>

- [Overview](#kinova-gen3-7-dof)
- [3D Printing Files](#3d-printing-files)
- [Simulation Environment](#simulation-environment)
- [Robot Description](#robot-description)
- [CORTEX Configuration](#cortex-configuration)
- [Hardware Components](#hardware-components)
  - [Driver & Control Interface](#driver--control-interface)
  - [Sensors](#sensors)
  - [Control Systems](#control-systems)
- [Quick Links](#quick-links)

</details>

---

## 3D Printing Files

The custom gripper fingers for the Kinova Gen3 were printed on a **Bambu Lab X1E** using **Recycled PLA** from [SmartMaterials3D](https://www.smartmaterials3d.com/pla-recycled).  
The complete `.3mf` project file is available here: [kinova.3mf](print/kinova.3mf)

---

## Simulation Environment

For virtual testing and development, use the official **[webots-p3bot bridge](https://github.com/robocomp/webots-p3bot)**, which provides seamless Webots integration for simulation, perception, and control pipelines.

---

## Robot Description

The kinematic and visual model of the Kinova Gen3 7-DOF is available in two standard formats for simulation and integration:

| Format | File Path | Purpose |
|--------|-----------|---------|
| URDF | [gen3_robotiq_2f_85.urdf](urdf/gen3_robotiq_2f_85.urdf) | Standard robot description format for ROS, Gazebo, and MoveIt integration |
| Proto | [KinovaGen3.proto](proto/KinovaGen3.proto) | Simulation-ready model definition optimized for Webots and custom physics engines |

These files define the arm's link hierarchy, joint configurations, collision meshes, and visual representations. Verify that they match your physical build before deployment.

---

## CORTEX Configuration

The runtime configuration for the Kinova Gen3 arm is managed through the CORTEX framework. All component parameters and network bindings are available in:

[cortex/kinovaGen3.json](cortex/kinovaGen3.json)
---

## Hardware Components

### Driver & Control Interface
- **Driver**: [kinova_controller_cpp](https://github.com/robocomp/manipulation_kinova_gen3/tree/P3Bot/agents/kinova_controller_cpp)

### Sensors

| Sensor Type | Model | RoboComp Component |
|-------------|-------|-------------------|
| Stereo Depth Camera | Intel RealSense D435i | [zed_component](https://github.com/robocomp/robocomp-shadow/tree/main/insect/zed_component) |

### Control Systems

Two primary control modes are available:

1. **Full Body Coordination**  
   Use the **[body_controller](https://github.com/robocomp/manipulation_kinova_gen3/tree/P3Bot/agents/body_controller)** component to synchronize mobile base motion with arm manipulation.

2. **Arm-Only Control (VR)**  
   Leverage the **[armController](https://github.com/alfiTH/robocomp-p3bot/tree/main/components/armController)** component for precise, low-latency arm control via VR controllers.

---

## Quick Links

| Resource | Link |
|----------|------|
| 3D Model (`.3mf`) | [kinova.3mf](print/kinova.3mf) |
| Webots Simulation | [webots-p3bot bridge](https://github.com/robocomp/webots-p3bot) |
| Protocol Buffer | [KinovaGen3.proto](proto/KinovaGen3.proto) |
| Robot Description (URDF) | [gen3_robotiq_2f_85.urdf](urdf/gen3_robotiq_2f_85.urdf) |
| RoboComp Framework | [GitHub Organization](https://github.com/robocomp) |

---
