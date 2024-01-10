# Advanced Kalman Filtering and Sensor Fusion Simulation

Welcome to the Advanced Kalman Filtering and Sensor Fusion Simulation exercise project. In this project, you will be developing the source code for a number of different types of Kalman Filters which are used to estimate the navigation state of a 2D vehicle problem; such as that would be found on a self-driving car!

![AKFSF-Simulation](/AKFSF-Simulation.gif)

This README is broken down into the following sections:

- [Setup](#setup) - the environment and code setup required to get started and a brief overview of the project structure.
- [The Tasks](#the-tasks) - the tasks you will need to complete for the project

## Setup

This project will use the Ubuntu 64 20.04.2.0 LTS VM C++ development environment that is setup for this course. (Refer to the Setting up the Development Environment Lesson) Please follow the steps below to compile the simulation.

0.  Install the dependencies

```
sudo apt install libeigen3-dev libsdl2-dev libsdl2-ttf-dev
```

1.  Clone the repository

```
git clone https://github.com/technitute/AKFSF-Simulation-CPP.git
```

2.  Setup the cmake build

```
cd AKFSF-Simulation-CPP
mkdir build
cd build
cmake ../
```

3.  Compile the code

```
make
```

3.  You should now be able to and run the estimation simulator

```
./AKFSF-Simulation
```

### Project Structure

There are 3 main files of interest:

- kalmanfilter_lkf.cpp
- kalmanfilter_ekf.cpp
- kalmanfilter_ukf.cpp

To use one of the filter files, replace the `kalmanfilter.cpp` file with the one of interest.

## Simulation Operation

The simulation can be run with different motion and sensor profiles to test the different scenarios and evaluate how the filter performs with different conditions. The different profiles can be activated pressing the number keys 1-9,0, to active the corresponding profile.

### Motion Profiles

- 1 - Constant Velocity + GPS + GYRO + Zero Initial Conditions
- 2 - Constant Velocity + GPS + GYRO + Non-zero Initial Conditions
- 3 - Constant Speed Profile + GPS + GYRO
- 4 - Variable Speed Profile + GPS + GYRO
- 5 - Constant Velocity + GPS + GYRO + LIDAR+ Zero Initial Conditions
- 6 - Constant Velocity + GPS + GYRO + LIDAR + Non-zero Initial Conditions
- 7 - Constant Speed Profile + GPS + GYRO + LIDAR
- 8 - Variable Speed Profile + GPS + GYRO + LIDAR
- 9 - Real life sim
- 0 - Real life sim (with No Lidar Data Association)
