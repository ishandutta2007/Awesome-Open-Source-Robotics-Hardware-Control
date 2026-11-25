# Awesome-Open-Source-Robotics-Hardware-Control

# Awesome Open Source Robotics & Hardware Control

> A curated list of top Open Source Robotics and Hardware Control platforms — both SaaS/Hosted commercial robotics platforms and open-source alternatives for robot fleets, simulation, control, and physical AI experimentation.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [AWS RoboMaker](#aws-robomaker)
  - [NVIDIA Isaac Sim](#nvidia-isaac-sim)
  - [Formant](#formant)
  - [InOrbit](#inorbit)
  - [Viam](#viam)
  - [Freedom Robotics](#freedom-robotics)
  - [Foxglove](#foxglove)
- [Open-Source Software](#-open-source-software)
  - [ROS 2](#ros-2)
  - [Open-RMF](#open-rmf)
  - [Foxglove Studio (Open Source)](#foxglove-studio-open-source)
  - [Microduck](#microduck)
  - [OpenCat](#opencat)
  - [TNY-360](#tny-360)
  - [Google Cloud Robotics Core](#google-cloud-robotics-core)
  - [Open Dynamic Robot Initiative](#open-dynamic-robot-initiative)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted robotics and hardware control platforms. These are not open-source but are included as reference points for feature comparison.

### AWS RoboMaker
**Type:** Cloud robotics development and simulation
AWS RoboMaker provides a managed service for robot development, simulation, and deployment, integrating with ROS and AWS services for ML, logging, and monitoring. It is positioned for teams wanting to build and test robotics applications in the cloud without managing infrastructure.

### NVIDIA Isaac Sim
**Type:** Robotics simulation and synthetic data generation
Isaac Sim provides a high-fidelity simulation environment built on NVIDIA Omniverse for developing and testing robots in physically accurate virtual worlds. It supports synthetic data generation for training perception models and sim-to-real transfer.

### Formant
**Type:** Robot fleet operations and data management
Formant provides a cloud platform for robot fleet observability, teleoperation, data collection, and incident response. It is positioned for commercial robotics companies needing to operate and monitor deployed fleets at scale.

### InOrbit
**Type:** RobOps platform for heterogeneous robot fleets
InOrbit provides a cloud-based Robot Operations (RobOps) platform for orchestrating, monitoring, and analyzing heterogeneous robot fleets across sites. It is positioned for organizations deploying multiple robot types needing unified fleet visibility.

### Viam
**Type:** Robotics platform for hardware control and fleet management
Viam provides a cloud platform for building, configuring, and managing robots, with hardware abstraction, fleet management, and data capture. It is positioned for developers wanting a managed platform for robot control without building infrastructure.

### Freedom Robotics
**Type:** Robot fleet management and teleoperation
Freedom Robotics provides cloud-based fleet management, teleoperation, and monitoring for commercial robots. It is positioned for robotics companies needing remote visibility and control over deployed units.

### Foxglove
**Type:** Robotics data visualization and observability
Foxglove provides a commercial platform for visualizing robotics data, with data search, session management, events, and fleet observability. Its SDK is open-source and supports Python, C++, and Rust, enabling direct WebSocket connections for real-time visualization without middleware [citation:4].

---

## 🟩 Open-Source Software

Self-hosted, community-driven robotics and hardware control tools. The open-source ecosystem spans **middleware frameworks**, **fleet orchestration systems**, **visualization tools**, **open hardware platforms**, and **research initiatives**.

### ROS 2
**Stack:** C++ / Python | **License:** Apache-2.0
ROS 2 (Robot Operating System 2) is the dominant open-source robotics middleware, providing a modular framework for building robot applications with reusable components and message-passing infrastructure [citation:3]. It addresses ROS 1 limitations through DDS middleware for decentralized discovery, improved real-time support, security primitives, and multi-robot scalability [citation:3]. The ecosystem includes MoveIt2 for manipulation, Nav2 for navigation, and micro-ROS for microcontrollers, with an open-access database indexing over 7,300 ROS-related publications [citation:3].  
**Best for:** Any robotics team needing the industry-standard open-source middleware for perception, planning, control, and multi-robot coordination.

### Open-RMF
**Stack:** C++ / Python | **License:** Apache-2.0
Open-RMF (Open Robotics Middleware Framework) is an open-source framework for **heterogeneous multi-robot fleet coordination** in shared environments, acting as a traffic controller that manages task allocation, conflict avoidance, and infrastructure interoperability (doors, elevators) [citation:12]. Key capabilities include task auctioning where fleet adapters bid on tasks based on cost, resource negotiation for traffic conflicts, shared traffic scheduling, and RMF-Web dashboards for visualization and control [citation:12]. Ready-made fleet adapters exist for some manufacturers, with APIs and a template for developing new ones [citation:12].  
**Best for:** Facilities deploying multiple robot brands (warehouses, hospitals, campuses) that need a vendor-neutral fleet coordination layer.

### Foxglove Studio (Open Source)
**Stack:** TypeScript / C++ | **License:** MPL-2.0
Foxglove Studio is the open-source core of the Foxglove platform, providing a visualization and debugging environment for robotics data. The **Foxglove SDK** is open-source and enables direct WebSocket connections to visualize multimodal data cross-platform (Python, C++, Rust) without relying on any middleware, with easy MCAP recording [citation:4]. It supports rich panels including 3D visualization, plots, logs, and data search across MCAP files.  
**Best for:** Teams wanting a powerful open-source robotics visualization tool that works with any middleware or directly via the SDK.

### Microduck
**Stack:** Open-source SDK / MuJoCo / Python | **License:** Open Source (software) / Proprietary (hardware)
Microduck is a 25cm open-source biped robot created by Pollen Robotics (Hugging Face) for physical AI and reinforcement learning experimentation [citation:1][citation:7]. The **software stack is open source**, including the SDK, simulation environment, and RL training stack on GitHub—developers train policies in MuJoCo, deploy them to the robot, and share behaviors [citation:7][citation:13]. **Important:** The hardware design files are **not open source**—Pollen explicitly asks that it not be described as open-source hardware [citation:13]. The robot has 15 motors, camera, LiDAR, IMUs, and runs on a Rockchip RK3566 with 1GB RAM [citation:1]. Pre-orders at $399 with deliveries targeted before Christmas 2026 [citation:1].  
**Best for:** Developers and researchers wanting an affordable physical platform for reinforcement learning and sim-to-real experimentation, accepting closed hardware with an open software stack.

### OpenCat
**Stack:** Arduino / Raspberry Pi / C++ / Python | **License:** Open Source (per repository)
OpenCat is an open-source quadruped robot framework from Petoi, powering the Bittle robot dog and Nybble robot cat platforms [citation:14]. It handles gait coordination, servo control, and IMU integration, with multi-language support (C/C++, Python, block-based coding) and compatibility with Arduino and Raspberry Pi [citation:14]. The framework supports sensor integration (cameras, touch, IMUs, ultrasonic), sim-to-real RL experiments, and ROS-compatible SLAM/navigation pipelines [citation:14]. Used in K-12 education, university research, and maker spaces worldwide.  
**Best for:** Educators, students, and researchers wanting an affordable, hackable quadruped platform for teaching and experimenting with robotics programming and AI.

### TNY-360
**Stack:** ESP32-S3 / C++ / FreeCAD | **License:** CC BY-NC-SA 4.0
TNY-360 is an open-source quadruped robot with **complete hardware and firmware files** publicly available on GitHub, including CAD files, PCB layouts, bill of materials, and ESP-IDF firmware [citation:2]. It uses 12 modified MG996R servos with custom op-amp buffer circuits for closed-loop position feedback, an ESP32-S3 managing control with a 200Hz control loop, and sensors including OV2640 camera, VL53L0X ToF, and MPU6050 IMU [citation:2]. **Important:** The CC BY-NC-SA license restricts commercial reuse [citation:2].  
**Best for:** Makers and educators wanting a fully open hardware quadruped design they can build, modify, and learn from, accepting the non-commercial license.

### Google Cloud Robotics Core
**Stack:** Go / Kubernetes / Terraform | **License:** Apache-2.0
Google's Cloud Robotics Core is an open-source platform providing infrastructure for building and running robotics solutions, including application packaging and distribution, secure bidirectional robot-cloud communication, and access to Google Cloud services (ML, logging, monitoring) [citation:6]. It runs on Google Kubernetes Engine (GKE) and is explicitly **pre-alpha** with support limited to early access partners—no stability or support guarantees are made [citation:6].  
**Best for:** Developers wanting to experiment with Google's cloud robotics infrastructure, accepting pre-alpha maturity and limited support.

### Open Dynamic Robot Initiative
**Stack:** C++ / Python | **License:** BSD (various)
The Open Dynamic Robot Initiative provides open-source hardware and software for torque-controlled robots, including the Solo Quadruped master board, TriFinger robot drivers, simulation environments, and camera drivers [citation:8]. Repositories include robot fingers, simulation packages, object tracking, and an open motor driver initiative for brushless motors [citation:8]. The project is actively maintained with BSD-licensed code across 41 repositories.  
**Best for:** Researchers and advanced developers working with torque-controlled legged robots and manipulation platforms, wanting open hardware and software foundations.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Hardware | Software | Self-Hosted | Best For |
|----------|---------|-------|----------|----------|-------------|----------|
| **AWS RoboMaker** | Proprietary | Cloud | ❌ | ✅ | ❌ | Cloud simulation + deployment |
| **NVIDIA Isaac Sim** | Proprietary | Cloud/Desktop | ❌ | ✅ | (Desktop) | High-fidelity simulation |
| **Formant** | Proprietary | Cloud | ❌ | ✅ | ❌ | Fleet ops + data management |
| **InOrbit** | Proprietary | Cloud | ❌ | ✅ | ❌ | Heterogeneous fleet orchestration |
| **Foxglove** | Proprietary | Cloud | ❌ | ✅ | (Desktop) | Data visualization + observability |
| **ROS 2** | Apache-2.0 | C++/Python | ❌ | ✅ | ✅ | Industry-standard middleware |
| **Open-RMF** | Apache-2.0 | C++/Python | ❌ | ✅ | ✅ | Multi-robot fleet coordination |
| **Foxglove Studio** | MPL-2.0 | TypeScript | ❌ | ✅ | ✅ | Open-source visualization |
| **Microduck** | Open Source (SW) | Python/MuJoCo | Proprietary | ✅ | ✅ | RL physical AI platform |
| **OpenCat** | Open Source | Arduino/Pi | ✅ | ✅ | ✅ | Affordable quadruped education |
| **TNY-360** | CC BY-NC-SA | ESP32/C++ | ✅ | ✅ | ✅ | Fully open quadruped build |
| **Cloud Robotics Core** | Apache-2.0 | Go/K8s | ❌ | ✅ | ✅ | Google Cloud robotics (pre-alpha) |
| **Open Dynamic Robot** | BSD | C++/Python | ✅ | ✅ | ✅ | Torque-controlled research robots |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source robotics or hardware control tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The open-source robotics landscape is **anchored by ROS 2** as the dominant middleware, with **Open-RMF** providing the fleet coordination layer for multi-robot environments [citation:3][citation:12]. For **visualization**, Foxglove Studio offers a powerful open-source option with an SDK that works across middleware [citation:4]. For **hardware experimentation**, Microduck provides an affordable physical AI platform with open software (but closed hardware) [citation:13], while OpenCat and TNY-360 offer fully open hardware designs for education and research [citation:2][citation:14]. Google's Cloud Robotics Core and the Open Dynamic Robot Initiative serve more specialized research and cloud infrastructure needs [citation:6][citation:8]. No single open-source project replicates the full managed convenience of AWS RoboMaker or Formant, but these tools cover the core middleware, orchestration, visualization, and hardware control workflows for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
