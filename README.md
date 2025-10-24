Nice — I pulled your uploaded script `CKF_Adversary (3).py`. 
Below I propose a concise repo name + one-line description and a ready-to-paste `README.md`, plus helpful git/Windows commands (so you won’t hit the same `git add` error again).

---

# Suggested repo name

**`ckf-adversary-robotarium`**

# Short GitHub description

`CKF-based adversary-aware state estimation & control demo for multi-UGV Robotarium simulations.`

---

# README.md (copy & paste)

````markdown
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
````

> **Note:** `rps.robotarium` (and `rps.utilities.*`) is Robotarium-specific and may require cloning/installing the Robotarium Python client or using the Robotarium SDK from their repository. Please follow Robotarium installation docs if you plan to run on the Robotarium hardware or local simulator.

---

## Installation

1. Clone repo:

```bash
git clone https://github.com/<your-username>/ckf-adversary-robotarium.git
cd ckf-adversary-robotarium
```

2. Create virtual environment and install deps:

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate

pip install -r requirements.txt
```

3. Install Robotarium client per its instructions (if needed).

---

## Quick start / Usage

1. Rename the script to remove spaces:

```bash
# Windows PowerShell example (from folder where file is located)
Rename-Item "CKF_Adversary (3).py" ckf_adversary.py
```

2. Run:

```bash
python ckf_adversary.py
```

If the script requires Robotarium simulation or specific initialization, use the appropriate flags or edit configuration constants near the top of the script (e.g., `CONFIG["TOTAL_ROBOTS"]`, `CONFIG["num_steps"]`, etc.).

---

## Running with Git (Windows example)

If your file currently sits at `C:\Users\karga\Tohid66161.github.io\CKF_Adversary (3).py` and your git repo is at `C:\Users\karga\ckf-adversary-robotarium`:

```powershell
# Move/rename file into your repo
Move-Item "C:\Users\karga\Tohid66161.github.io\CKF_Adversary (3).py" "C:\Users\karga\ckf-adversary-robotarium\ckf_adversary.py"

# Change to repo folder
cd C:\Users\karga\ckf-adversary-robotarium

# Initialize git (if not already)
git init
git remote add origin https://github.com/<your-username>/ckf-adversary-robotarium.git

# Add, commit, push
git add ckf_adversary.py README.md requirements.txt .gitignore
git commit -m "Add CKF adversary Robotarium simulation script + README"
git branch -M main
git push -u origin main
```

If `git add` previously failed with `pathspec ... did not match any files`, it means either the path was wrong or the file was not in the current working directory. Using the `Move-Item` (rename + move) ensures the file is in your repo before `git add`.

---

## Recommended `requirements.txt`

```
numpy
scipy
matplotlib
pandas
```

(If you know the Robotarium pip package name, add it here; otherwise follow their install guide.)

---

## Recommended `.gitignore`

```
venv/
__pycache__/
*.pyc
*.log
*.ipynb_checkpoints
outputs/
```

---

## Notes & next steps

* I recommend renaming the file to `ckf_adversary.py` (no spaces) and placing it in the repo root or `src/`.
* Consider splitting the long script into modules (`estimation.py`, `control.py`, `sim.py`, `utils.py`) for maintainability.
* Add a small `examples/README.md` describing how to run single scenarios (e.g., demo with 10 robots, demo with DoS enabled).

---

If you want, I can:

* produce the actual `README.md` file text in the repo format (I already did — ready to paste),
* generate a `requirements.txt` and `.gitignore` exact contents for you to paste,
* or produce a commit-ready `git` command sequence customized to the exact paths you tell me.

Which of those would you like next? (I can paste the `requirements.txt` and `.gitignore` contents ready-to-add.)
