# robots Repository

This repository contains the complete software stack, kinematic models, simulation environments, and CORTEX configurations for the **P3Bot** and its integrated **Kinova Gen3 7-DOF robotic arm**. All components are designed to work within the RoboComp framework and support seamless deployment across hardware and simulated environments.

<details>
<summary><strong>Table of Contents</strong></summary>

- [Repository Structure](#repository-structure)
- [Robot Documentation](#robot-documentation)
- [Key Resources](#key-resources)
- [Getting Started](#getting-started)
- [Framework & Dependencies](#framework--dependencies)
- [License & Contributing](#license--contributing)

</details>

---

## Repository Structure

```
.
├── P3Bot/                  # Mobile base documentation and components
│   ├── README.md           # Detailed setup, hardware specs, and control modes
│   ├── urdf/               # URDF model for ROS/Gazebo integration
│   ├── proto/              # Webots simulation definition
│   └── cortex/             # CORTEX runtime configuration
├── KinovaGen3/             # Arm documentation and components
│   ├── README.md           # Gripper specs, driver setup, and control interfaces
│   ├── urdf/               # URDF model with Robotiq 2F-85 gripper
│   ├── proto/              # Webots simulation definition
│   └── cortex/             # CORTEX runtime configuration
├── print/                  # 3D printing files (.3mf) for custom parts
└── images/                 # Documentation assets and robot photos
```

## Robot Documentation

Each platform has dedicated documentation covering hardware specifications, control architectures, simulation setup, and deployment guides:

- **[P3Bot](P3Bot/README.md)**  
    Omnidirectional drive base with dual Kinova Gen3 arms. Includes motor controller integration, LiDAR filtering, VR arm control, and full-body coordination.

- **[Kinova Gen3 7-DOF Arm](KinovaGen3/README.md)**  
    Detailed guide for the 7-DOF manipulator with custom 85mm parallel gripper. Covers kinematic modeling, sensor integration, and VR/teleoperation control modes.

---

## Key Resources

| Resource | Path / Link |
|----------|-------------|
| P3Bot URDF | [P3Bot/urdf/P3Bot.urdf](P3Bot/urdf/P3Bot.urdf) |
| Kinova Gen3 URDF | [KinovaGen3/urdf/gen3_robotiq_2f_85.urdf](KinovaGen3/urdf/gen3_robotiq_2f_85.urdf) |
| Webots Simulation Bridge | [webots-p3bot bridge](https://github.com/robocomp/webots-p3bot) |
| P3Bot CORTEX Config | [P3Bot/cortex/P3bot.json](P3Bot/cortex/P3bot.json) |
| Kinova Gen3 CORTEX Config | [KinovaGen3/cortex/kinovaGen3.json](KinovaGen3/cortex/kinovaGen3.json) |

---

## Framework & Dependencies

This repository is built on top of the following core technologies:
- **[RoboComp](https://github.com/robocomp)** – Component-based robotics framework
- **[Webots](https://cyberbotics.com/)** – Robot simulation environment
- **CMake & C++23** – Build system and language standard
Ensure all dependencies are installed before compiling components. Refer to each robot's README for version-specific requirements.