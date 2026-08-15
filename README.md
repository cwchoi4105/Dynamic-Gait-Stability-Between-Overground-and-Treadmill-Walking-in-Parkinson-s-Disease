# Dynamic-Gait-Stability-Between-Overground-and-Treadmill-Walking-in-Parkinson-s-Disease
Discrete analysis vs. Time-continuous statistical parametric mapping (SPM) analyses.

Although dynamic gait stability is known to vary across gait cycle phases, most studies have relied on discrete analyses, and phase-specific patterns remain untested with time-continuous analyses. This study compared dynamic gait stability between overground walking (OG) and treadmill walking (TM) at self-selected speeds in people with Parkinson's disease (PwPD) using discrete analysis and statistical parametric mapping (SPM), including gait-phase-normalised (GPN) SPM. Sixteen PwPD completed both OG and TM conditions. Feasible stability region (FSR)-based dynamic gait stability, centre of mass (COM) position, and COM velocity were analysed as discrete values and continuous time series. Discrete analysis detected no significant difference in stability between OG and TM at touchdown or liftoff, despite significant differences in COM position and velocity. In contrast, SPM showed that stability was significantly greater during OG than during TM across the entire analysis interval (ipsilateral-to-contralateral touchdown, 0–100%; p = 0.004). GPN analysis showed that this difference was predominantly located in the single-stance phase (14–100%; p = 0.025), while the double-stance phase showed a difference confined to the initial portion (0–18%; p = 0.049). SPM analysis captured stability differences that discrete analysis at specific gait events did not detect, and GPN further enabled within-phase comparisons.

<img width="3013" height="1685" alt="Image" src="https://github.com/user-attachments/assets/c2219f74-485e-4560-a075-f5491d784bef" />

# Lower Limb Obstacle Avoidance Task With IMUs

This is a motor-control task in which participants perform lower-limb movements (e.g., knee flexion and extension) while Inertial Measurement Units (IMUs) control a cursor on a screen. Participants move the cursor between two targets, and obstacles may appear during the task. When an obstacle appears, participants are instructed to avoid it.

This code uses [MotionNode](https://www.motionnode.com/) sensors and draws heavily on the MotionNode SDK. The task was created by Phil Desrochers for the Motor Development Lab at Boston University.

> **Note:** This project was developed during my first experience using Python, so the code may not be optimized.

## Purpose

The purpose of this task is to investigate how participants adjust online lower-limb movements as task constraints change.

## Repository Contents

| File | Description |
|---|---|
| `README.md` | Provides information about the task, repository files, and setup instructions. |
| `LL_obstacle_avoidance_task_IMU.py` | Main script used to run the task. |
| `MotionSDK.py` | MotionNode-provided file containing functions used to read data from the IMUs. |
| `Calibration.py` | Calibrates for variation in IMU placement on the participant's leg and for the participant's perceived straight-ahead knee flexion/extension position. |
| `trial_conditions_example.txt` | Contains condition numbers for each trial in a practice block. The number of lines determines the number of trials, and each line specifies the condition for one trial. |
| `trial_conditions.txt` | Contains condition numbers for each trial in an experimental block. The number of lines determines the number of trials, and each line specifies the condition for one trial. |
| `LICENSE` | Contains the Creative Commons license for this project. |

## Trial Conditions

This task includes five trial types:

| Condition | Description |
|---:|---|
| 0 | No obstacle |
| 1 | Obstacle appears before the cue |
| 2 | Obstacle appears with the cue |
| 3 | Obstacle appears at movement onset |
| 4 | Obstacle appears at 20% of movement amplitude |

The purpose of these conditions is to examine how the motor system modifies ongoing movements when new information becomes available at different stages of motor planning and execution.

In `trial_conditions.txt` and `trial_conditions_example.txt`, each line contains one condition number corresponding to one trial.

## Prerequisite Software

This task is run using Python. Installing the latest version of [Anaconda](https://www.anaconda.com/products/individual) is recommended.

The task also requires [Pygame](https://www.pygame.org/), a Python module for developing simple graphical applications.

To install Pygame:

1. Open the Anaconda Prompt.
2. Enter the following command:

```bash
pip install pygame
```

## Downloading the Task

Download this repository as a ZIP file or clone it to your computer:

```bash
git clone <repository-url>
```

Although the task may be stored on a laboratory drive, it should be run from a local directory rather than directly from the drive. Running the task from a network drive may cause lag because the program must read and write data over an internet connection.
