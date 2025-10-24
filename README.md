# CKF Adversary — Robotarium Simulation

**Short description:** Cubature Kalman Filter (CKF) multi-robot simulation with adversary models (FDI / DoS), event-triggered communication, control barrier functions and basic path tracking (Stanley/Pure Pursuit) for Robotarium experiments.

---

## Overview
This project contains a CKF-based state estimation and control simulation for a multi-UGV team running in the Robotarium environment. It includes event-triggered communication logic, shadow measurements, attack simulation (FDI and DoS), control barrier functions (CBF) to avoid collisions, and leader/follower controllers (Stanley/pure pursuit style). The main file is `CKF_Adversary (3).py`. :contentReference[oaicite:0]{index=0}

---

## Features
- Cubature Kalman Filter (CKF) prediction & measurement updates
- Event-triggered communication with adaptive thresholds
- Shadow-edge sensing and shadow-range measurement handling
- Attack simulation:
  - FDI (False Data Injection) on sensing
  - DoS (Denial of Service) on communications
- Collision avoidance via Control Barrier Functions (CBF)
- Leader (Stanley) and follower control policies
- Visualization using Robotarium plotting utilities and Matplotlib

---

## Requirements
Tested with (minimum):
- Python 3.8+
- numpy
- scipy
- matplotlib
- pandas
- Robotarium Python API (rps.robotarium) and rps utilities (transformations, barrier_certificates, controllers, graph)
- logging (stdlib)

Install via pip (example):
```bash
pip install numpy scipy matplotlib pandas
# robotarium library may be provided by your Robotarium / rps package — install according to your Robotarium instructions
