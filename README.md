# CKF Adversary — Robotarium Multi-UGV Demo

**One-liner:** CKF-based (Cubature Kalman Filter) adversary-aware state estimation and control demo for multi-UGV Robotarium simulations — includes event-triggered updates, shadow-edges, CBF collision avoidance, and simple DoS/FDI adversary models.

---

## Contents
- `ckf_adversary.py` — main simulation script (rename from `CKF_Adversary (3).py` to avoid spaces).
- `requirements.txt` — Python dependencies.
- `examples/` — optional folder for saved runs, logs, sample plots.
- `LICENSE` — MIT recommended (or whichever you prefer).
- `README.md` — this file.

---

## Features
- Cubature Kalman Filter (CKF) time/measurement updates.
- Event-triggered communication logic with adaptive thresholds.
- Support for shadow-edge measurements (shadow-range).
- Basic adversary modeling: DoS (communication) and FDI (measurement corruption).
- Leader-follower control policies (Stanley / Pure Pursuit + Control Barrier Functions).
- Robotarium integration for visualization.

---

## Requirements
Tested with Python 3.9+ — install packages below:

```text
numpy
scipy
matplotlib
pandas
logging
# Robotarium client (see note below)
