# redback-e-waste-battery-extraction-docs

Documentation for **Redback Operations, Project 7: E-Waste Battery Extraction**.

This project builds a robot that autonomously extracts lithium-ion batteries from end-of-life electronic devices. The current scope focuses on Samsung smartphones. This repository is the shared home for all research, design, and technical documentation produced by the project's three sub-teams: Robotics, Computer Vision, and Simulation.

---

## Project at a glance

| | |
|---|---|
| Goal | Safe, efficient, cost effective autonomous battery extraction from e-waste |
| Current focus device | Samsung smartphones |
| Physical platform | UFACTORY xArm 7 (7 DoF collaborative arm, in the Burwood lab) |
| Simulation platforms | Kinova Gen 3 and UR3 (primary sim targets), xArm 7 (physical validation) |
| Simulation strategy | Kinematic modelling in MATLAB, then physics accurate 3D in NVIDIA Isaac Sim |
| Success pillars | Safety, Sustainability, Affordability, Efficiency |

---

## Repository structure

```
.
├── README.md                        (this file, the project overview)
├── computerVision/
│   ├── README.md
│   └── Trimester 1 2026/
│       ├── Model Research Reprt.pdf
│       ├── makingNewAutomationBlender...pdf
│       └── new.pdf
├── robotics/
│   ├── README.md
│   ├── ResearchStudiesUsed/
│   ├── Cost_Analysis.pdf
│   ├── Robot_Platform_Feasibility_Report.pdf
│   └── Robotic_Arm_Evaluation_Report.pdf
└── simulation/
    └── README.md
```

Each sub-team owns its own top level folder and the documents inside it. Every folder has its own README that describes what that sub-team is responsible for and what its documents contain. Start at a sub-team's README to understand that stream, then open the individual documents.

---

## The three sub-teams

### Robotics
Owns arm selection, end-effector design, kinematics, motion planning, and the physical extraction workflow. Current documents cover the robotic arm evaluation (SCARA vs Delta vs 6-axis articulated), the platform feasibility comparison (Kinova Gen 3, xArm 7, UR3), and the bill of materials with cost analysis across the heating and cooling thermal configurations. Reference papers used for this research live in the ResearchStudiesUsed folder.

### Computer Vision
Owns battery and device detection, pose estimation, and the perception pipeline that feeds target poses to the Robotics team. Current documents live under Trimester 1 2026 and cover model research and automation work.

### Simulation
Owns the simulated environment (Isaac Sim and Gazebo), the URDF and configuration files, and kinematic modelling in MATLAB. Documents to be added as the environment is built.

---

## How the streams connect

The three sub-teams form one pipeline. Simulation provides the virtual environment and robot models. Computer Vision detects the battery and computes a target pose. Robotics plans a collision free path and drives the arm to that pose. If you are new to how ROS 2 and MoveIt! tie these together, read the shared ROS 2 overview (see the Computer Vision or Robotics READMEs) before diving into a specific stream.

---

## Working with this repository

### Editing on GitHub (easiest for small changes)
1. Open the file you want to change and click the pencil (edit) icon.
2. Make your edit.
3. Scroll to the bottom, write a short commit message describing the change, and click Commit changes.

### Adding a new document
1. Click Add file, then Create new file (or Upload files for a PDF).
2. To place it inside a sub-team folder, type the folder name followed by a slash before the file name, for example robotics/my-new-report.md. GitHub creates the folder path automatically.
3. Commit with a short message.

### Working from your computer (for larger changes)
```
git clone https://github.com/<owner>/redback-e-waste-battery-extraction-docs.git
cd redback-e-waste-battery-extraction-docs

git checkout -b my-change      (optional, work on a branch)
# add or edit files
git add .
git commit -m "Describe what you changed"
git push
```
If you worked on a branch, open a pull request on GitHub so the project lead can review before it merges into main.

---

## Conventions

Keep each document in its own sub-team folder. Use Markdown (.md) for written docs where possible, and store PDFs in the relevant sub-team folder. Put images and figures alongside the document that uses them, and link them with a relative path. Write clear commit messages that say what changed and why. Every folder needs at least one file to exist on GitHub, so keep a README in each.

---

*Redback Operations, Deakin University, Project 7: E-Waste Battery Extraction*
