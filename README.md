# Isaac-Sim-Tutorial
This repository is all about Isaac Sim Tutorial for Robot Simulation.

# Requirements

This repository was tested on Ubuntu 22.04, Nvidia Driver 535, Cuda 12.4, Python 3.10 and ROS2 Humble. 

# Installation

The workstation installation of Isaac Sim is recommended for users who wants to run Isaac Sim as a GUI application on a Linux workstation with a GPU.

## Workstation Setup
Ensure your local workstation meets the System Requirements and Driver Requirements for running NVIDIA Isaac Sim.

- Install Visual Studio Code to view and debug source code.

- Download the 4.5 version of Isaac Sim to the default Downloads folder from this [website](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/download.html).

- Unzip the package to the recommended Isaac Sim root folder and Run the Isaac Sim App Selector.

- Run the commands below in Terminal for Linux.

```
mkdir ~/isaacsim
cd ~/Downloads
unzip "isaac-sim-standalone@4.5.0-rc.36+release.19112.f59b3005.gl.linux-x86_64.release.zip" -d ~/isaacsim
cd ~/isaacsim
./post_install.sh
./isaac-sim.selector.sh
```

- The Isaac Sim app can be run directly via command line with `isaac-sim.bat` or `./isaac-sim.sh`.

- The post_install` script is run to create a symlink to the extension_examples folder for the tutorials.

- Nucleus, Cache and Hub is not needed to run Isaac Sim.

- Hub Workstation Cache is not fully supported in Isaac Sim 4.5.0 and performance using Hub may vary.

Local Assets Packs

Isaac Sim Launch Scripts for additional scripts like the warmup script to pre-warm the shader cache before runnign Isaac Sim.

Isaac Sim App Selector
The Isaac Sim App Selector is a mini-windowed app that helps run Isaac Sim in different modes.

Click START to run the Isaac Sim main app.

Isaac Sim First Run

Proceed to Getting Started Tutorials to begin the first Basic Tutorial.

The first run of the Isaac Sim app takes some time to warm up the shader cache.

To run Isaac Sim with a fresh config, use the --reset-user flag. This flag can be entered in the Extra Args section of the Isaac Sim App Selector or when running Isaac Sim in command line.

## Docker setup

# Resources
- Using Isaac Sim with ROS2: A Step-By-Step Guide [[video]](https://www.youtube.com/watch?v=L1rpxRm0Q1w)
- UR5 Inverse Kinematics + ROS2 Explained (Nvidia Omniverse Isaac Sim) [[video]](https://www.youtube.com/watch?v=DzKHEtwAOLU)
- Simulation took Control of my Robot Arm (NVIDIA Isaac Sim) [[video]](https://www.youtube.com/watch?v=Eb2zuQxOBlY)
- How to import my manipulator in Isaac Sim [[video]](https://www.youtube.com/watch?v=kRAZZ5OPZyM)
- How to Use MoveIt with Isaac Sim: A Step-by-Step Guide [[video]](https://www.youtube.com/watch?v=pGje2slp6-s)
- How to Utilize LeRobot, Isaac Sim and ROS2 [[video]](https://www.youtube.com/watch?v=eO5wMzw9LeQ)
