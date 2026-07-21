# 🌌 Incursion-2: A Black Hole Effect and Big Bang Simulation

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![OpenGL Version](https://img.shields.io/badge/OpenGL-3.3%20Core-orange.svg)](https://www.opengl.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

A high-fidelity Python + OpenGL 3.3 Core Profile simulation engine modeling general relativity visual phenomena, accretion disk dynamics, N-body gravity orbital mechanics, space-time grid deformation, and an 18-phase cosmic lifecycle from gravitational collapse to universe rebirth.

## 👥 Team Members

| Name | Role | Profile |
| :--- | :--- | :--- |
| Md. Raihan Molla | Contributor | [LinkedIn](https://www.linkedin.com/in/raihanx009/) |
| Md. Emam Zafor Saadik | Contributor | [LinkedIn](https://www.linkedin.com/in/zafor-saadik) |
| Samia Sultana | Contributor | [LinkedIn](https://www.linkedin.com/in/samia-sultana-47297a276/) |

---

## 🎬 Project Preview

### 🖼️ Simulator Screenshot
![Simulator Preview](image.png)

### 📹 Simulation Demo
<p align="center">
  <video src="Incursion_Demo.mp4" width="100%" controls loop muted></video>
</p>

---

## 🤝 Team Project & My Contributions

This repository is a fork of the original team project, developed collaboratively for an academic purpose. My primary responsibilities included:

**Physics Implementation**
- Implemented and refined core physics algorithms for gravitational interactions.
- Contributed to the N-body gravitational simulation using Velocity Verlet integration.
- Assisted in developing orbital mechanics, gravitational collapse behavior, and black hole interaction logic.
- Participated in testing and tuning simulation parameters to improve realism and stability.

**Documentation**
- Contributed to writing and improving the project documentation.
- Helped prepare technical documentation explaining the simulation architecture, physics methodology, and project workflow.
- Improved project organization and README content for better usability and maintainability.

---

## 🚀 Key Features

- **Deferred Rendering & HDR Pipeline** — A Multi-Render Target (MRT) framebuffer utilizing 16-bit floating-point textures (`GL_RGBA16F`) to capture high-dynamic-range brightness without color clipping.
- **Gravitational Lensing** — Screen-space UV distortion post-process pass simulating light bending around the black hole, creating an analytical Einstein Ring.
- **Accretion Disk Physics** — 30,000 Keplerian orbiting point-sprites colorized dynamically by a black-body temperature approximation (10,000K–40,000K) with inspiral decay.
- **Tidal Spaghettification** — Real-time non-uniform geometric stretching along the radial axis and lateral compression, computed in vertex shaders as planets approach the event horizon.
- **Dynamic Space-Time Grid** — A deformable mesh in the XZ plane, deformed in real-time in the vertex shader based on localized mass density attractors.
- **Velocity Verlet Integration** — Second-order numerical integration solver simulating N-body gravity during collapse.
- **18-Phase State Machine** — A complete cosmic lifecycle:

  Normal Solar System Orbit → Approach & N-Body Collapse → Critical Merge Flash → Singularity Formation → Tidal Devouring → Hawking Evaporation → Big Bang Rebirth → Quark-Gluon Plasma → Dark Ages → First Stars & Galaxy Formation → Nebula & Protoplanetary Disk → New Terraform Earth Rebirth

- **Real-time HUD Controls** — Dear ImGui control panel to configure physics variables, camera modes, post-processing options, and trigger events.

---

## ⚙️ Quick Start

### 📋 Prerequisites
Python 3.10+ and a GPU supporting OpenGL 3.3 Core Profile.

### 📥 Installation
```bash
pip install -r blackhole_sim/requirements.txt
```

### 🎮 Running the Simulator
Run from the repository root directory:
```bash
python blackhole_sim/main.py
```

---

## 🕹️ Controls

| Control | Action |
| :--- | :--- |
| **Mouse Left Drag** | Orbit camera (in `ORBIT` camera mode) |
| **Mouse Scroll** | Zoom camera in / out |
| **Mouse Left Click** | Click on any planet/object to select and view real-time data |
| **SPACE** | Trigger Gravitational Collapse / Advance Phase |
| **R** | Reset simulation to initial state |
| **C** | Cycle camera modes (`Orbit` → `Follow Black Hole` → `Earth Focus` → `ISS Focus`) |
| **G** | Toggle Space-Time Grid visibility |
| **A** | Toggle Atmosphere rendering |
| **B** | Toggle Bloom post-processing effect |
| **ESC / Q** | Quit simulator |

---

## 📂 Project Structure
