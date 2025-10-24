# CKF Adversary — Robotarium Multi-Robot Simulation

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]()

**Repository name:** `ckf-adversary-robotarium`  
**Main script:** `ckf_adversary.py` (renamed from original)

---

## Overview
This repository provides a simulation platform for evaluating the robustness of multi-robot state estimation and control under **adversarial sensing and communication interference**. It integrates **Cubature Kalman Filter (CKF)**, **event-triggered communication**, **shadow sensing**, **Control Barrier Functions (CBF)**, and **leader–follower motion strategies** using the Robotarium environment.

This framework enables research on resilient autonomy for cyber-physical and multi-robot systems.

---

## Key Features
- **Cubature Kalman Filter (CKF)** for nonlinear state estimation
- **Event-triggered communication** to reduce bandwidth
- **Shadow-edge sensing** for indirect perception
- **Adversary modeling**
  - False Data Injection (FDI) adversary
  - Denial of Service (DoS) adversary
- **Safety via Control Barrier Functions**
- **Leader–Follower controllers** (Stanley / Pure Pursuit)
- Visualization + CSV logging for post-processing
- Configurable for replicable experiments

---

## Motivation
Autonomous multi-robot systems operating over wireless networks are vulnerable to degraded sensing and limited communications.  
This simulator enables the study of:
- Resilient estimation & control
- Safe coordination under adversarial effects
- Efficient communication policies

---

## Dependencies

| Package | Purpose |
|--------|---------|
| numpy, scipy | CKF and dynamics |
| matplotlib | Visualization |
| pandas | Experiment logging |
| tqdm (optional) | Progress indication |
| Robotarium API (optional) | Hardware/realistic sim integration |

Install example:
```bash
pip install numpy scipy matplotlib pandas tqdm
