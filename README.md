# MSight: Digital Infrastructure for Roadside Intelligence

## Overview

**MSight** is an open-source, full-stack digital infrastructure for roadside intelligence, developed by University of Michigan Transportation Research Institute (UMTRI). It enables real-time perception, tracking, prediction, and communication for transportation systems by integrating multi-sensor data streams with scalable edge–cloud architecture.

MSight is designed to serve as a foundational platform for next-generation transportation applications, including:

* 🚗 Cooperative perception (CP)
* ⚠️ Near-miss and conflict detection
* 📡 V2X communication and safety messaging
* 🧠 AI-driven traffic understanding and prediction


<p align="center">
  <img src="cover.jpg" alt="MSight Cover" width="800"/>
</p>


For more details, visit:

* 🌐 Official Website: [https://msight.um.city/](https://msight.um.city/)
* 📚 Documentation: [https://msight-user-docs.readthedocs.io/en/latest/](https://msight-user-docs.readthedocs.io/en/latest/)

---

## Architecture

MSight follows a modular, multi-repository architecture to support scalability, flexibility, and independent development of components.

This repository serves as the **entry point** ("front door") and integrates the core modules as submodules.

---

## Core Modules

### 🧱 [MSight_base](https://github.com/michigan-traffic-lab/MSight_base)

Provides the **fundamental data abstractions and utilities** for MSight's digital infrastructure.

Key features:

* Standardized object definitions: road users, points, trajectories, frames
* Data containers and lifecycle management
* Trajectory management system
* Visualization utilities for debugging and analysis

This layer defines the **canonical data schema** used across all MSight modules.

---

### ⚙️ [MSight_Core](https://github.com/michigan-traffic-lab/MSight_Core)

Implements the roadside **distributed system backbone** for real-world, scalable edge deployments.

Key features:

* Bag of Nodes framework
* High-performance pub/sub communication
* Data serialization and transport
* Deployment tools for edge system

This layer enables **low-latency, production-grade deployment** of MSight systems.

---

### 🎥 [MSight_Vision](https://github.com/michigan-traffic-lab/MSight_Vision)

Handles **2D sensor processing**, focusing on camera-based perception.

Supported sensors:

* RGB cameras
* Fisheye cameras
* Infrared cameras

Key features:

* Object detection pipelines
* Multi-camera processing
* Integration with downstream tracking and fusion modules

This module serves as the **visual perception front-end** of MSight.

---

### 🛰️ MSight_Lidar (🚧 Coming Soon)

This module will provide:

* 3D perception using LiDAR
* BEV-based fusion capabilities
* Integration with MSight_Core and MSight_base

> ⚠️ This repository is currently under development and not yet available.

---

## Getting Started

### Install from PyPI

Install modules based on your use case:

1. Base package (required)
```bash
pip install msight-base
```

2. Core runtime package (for deployment and edge workflows)
```bash
pip install msight-core
```

3. Vision package (for camera-based perception)
```bash
pip install msight-vision
```

LiDAR-based perception support will be available in the upcoming MSight Lidar module.

### Clone the repository

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/michigan-traffic-lab/MSight
```

If you already cloned the repository without submodules:

```bash
git submodule update --init --recursive
```

---

## Design Philosophy

MSight is built around several core principles:

* 🧩 **Modularity** — Each component is independently developed and maintained
* ⚡ **Real-time performance** — Optimized for low-latency edge deployment
* 🌍 **Scalability** — From single intersections to city-scale systems
* 🔗 **Interoperability** — Standardized data schemas and interfaces

---

## Contributing

We welcome contributions from the community. Please refer to individual submodules for contribution guidelines.

---

## License

This project is licensed under the [BSD 3-Clause License](./LICENSE).

Copyright (c) 2026, University of Michigan Transportation Research Institute (UMTRI), University of Michigan.

---

## Acknowledgements

Developed by the University of Michigan Transportation Research Institute (UMTRI), University of Michigan.

Main developers: Rusheng Zhang

---

## Notes

* This repository uses Git submodules. Make sure to clone with `--recurse-submodules`.
* Do not remove or ignore submodule directories.
