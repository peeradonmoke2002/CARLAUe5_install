# CARLAUe5_install
 guide to installation carla ver ue5


## Table of Contents
- [Installation](#installation)
- [Trubleshooting](#troubleshooting)


## Installation

**Setp 1**: Git clone the repository

```bash
git clone -b ue5-dev https://github.com/carla-simulator/carla.git CarlaUE5
```

**Step 2**: Get the Unreal Engine `5.5` repository

To build CARLA, you need to use a special version of Unreal Engine 5.5 made for CARLA. To access this version, connect your GitHub account to Epic Games by [clicking here](https://www.unrealengine.com/en-US/ue-on-github).


**Step 3**: set git local credential

```bash
code ~/.bashrc
```
Add the following line to the end of the file:

```bash
export GIT_LOCAL_CREDENTIALS=[Your_Username]@[Your_Token]
```
> Replace `[Your_Username]` and `[Your_Token]` with your actual GitHub username and personal access token.

Then, save the file and run the following command to apply the changes:


**Setp 4**: Run the following commands to build CARLA:

```bash
cd CarlaUE5
sudo -E ./CarlaSetup.sh
```
This will download and install Unreal Engine 5.5, install the prerequisites and build CARLA. It may take some time to complete and use a significant amount of disk space.




## Troubleshooting

### Cmake Error

If you face problems like this:

```bash
CMake Error at CMakeLists.txt:16 (cmake_minimum_required):
  CMake 3.27.2 or higher is required.  You are running version 3.22.1
```
You need to install a newer version of CMake. You can do this by following these steps:

