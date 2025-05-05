# Isaac Sim Tutorial
This repository is all about Isaac Sim Tutorial for Robot Simulation.

# Requirements

Isaac Sim 4.5 installation was tested on Ubuntu 22.04, Nvidia Driver 535, Cuda 12.4, Python 3.10 and ROS2 Humble. 

# Installation

The workstation installation of Isaac Sim is recommended for users who wants to run Isaac Sim as a GUI application on a Linux workstation with a GPU.

## Workstation Setup
Ensure your local workstation meets the System Requirements and Driver Requirements for running NVIDIA Isaac Sim.

Install Visual Studio Code to view and debug source code.
```bash
sudo snap install code
```
Download the 4.5 version of Isaac Sim to the default Downloads folder from this [website](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/download.html).

```bash
mkdir ~/isaacsim
```
Unzip the package to the recommended Isaac Sim root folder:
```
cd ~/Downloads
unzip "isaac-sim-standalone@4.5.0-rc.36+release.19112.f59b3005.gl.linux-x86_64.release.zip" -d ~/isaacsim
```
The post_install script is used to create a symlink to the extension_examples folder for the tutorials. Run the Isaac Sim App Selector:
```bash
cd ~/isaacsim
./post_install.sh
./isaac-sim.selector.sh
```

The Isaac Sim app can be run directly via command line with 
```bash
./isaac-sim.sh
```
Nucleus, Cache and Hub is not needed to run Isaac Sim. Hub Workstation Cache is not fully supported in Isaac Sim 4.5.0 and performance using Hub may vary.

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

# Troubleshooting Installation
You can see something like this during post-installation process:
```
An input-output memory management unit (IOMMU) appears to be enabled on this system.
On bare-metal Linux systems, CUDA and the display driver do not support IOMMU-enabled PCIe peer to peer memory copy.
If you are on a bare-metal Linux system, please disable the IOMMU. Otherwise you risk image corruption and program instability.
This typically can be controlled via BIOS settings (Intel Virtualization Technology for Directed I/O (VT-d) or AMD I/O Virtualization Technology (AMD-Vi)) and kernel parameters (iommu, intel_iommu, amd_iommu).
Note that in virtual machines with GPU pass-through (vGPU) the IOMMU needs to be enabled.
Since we can not reliably detect whether this system is bare-metal or a virtual machine, we show this warning in any case when an IOMMU appears to be enabled.
```
Disable IOMMU (for bare-metal systems only):

- Disable VT-d or AMD-Vi in BIOS Reboot

- Enter BIOS/UEFI (usually Del, F2, or Esc)

- Find Intel VT-d or AMD-Vi under advanced settings

- Disable it

- Save and reboot

# Resources
- Isaac Sim 4.5 & Isaac Lab 2.0 | Installation & Overview | NVIDIA Omniverse [[video]](https://www.youtube.com/watch?v=CLFjtuH2NAQ) 
- Using Isaac Sim with ROS2: A Step-By-Step Guide [[video]](https://www.youtube.com/watch?v=L1rpxRm0Q1w)
- UR5 Inverse Kinematics + ROS2 Explained (Nvidia Omniverse Isaac Sim) [[video]](https://www.youtube.com/watch?v=DzKHEtwAOLU)
- Simulation took Control of my Robot Arm (NVIDIA Isaac Sim) [[video]](https://www.youtube.com/watch?v=Eb2zuQxOBlY)
- How to import my manipulator in Isaac Sim [[video]](https://www.youtube.com/watch?v=kRAZZ5OPZyM)
- How to Use MoveIt with Isaac Sim: A Step-by-Step Guide [[video]](https://www.youtube.com/watch?v=pGje2slp6-s)
- How to Utilize LeRobot, Isaac Sim and ROS2 [[video]](https://www.youtube.com/watch?v=eO5wMzw9LeQ)
