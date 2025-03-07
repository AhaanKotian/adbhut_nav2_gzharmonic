# Ackermann Steering Vehicle Simulation in ROS2 with Gazebo Sim Harmonic

This project features the simulation of a custom vehicle with **Ackermann steering capabilities**, developed using **ROS2** and the **Gazebo Sim Harmonic environment**. The model integrates a variety of sensors and navigation tools for autonomous operation, making it one of the first implementations of an Ackermann steering vehicle in this simulation framework.

## Features

### 1. **Ackermann Steering**

- A custom vehicle model built with realistic Ackermann steering dynamics for accurate maneuverability.

### 2. **ROS2 Communication**

- All sensor data and control signals are fully integrated into the ROS2 ecosystem for seamless interoperability.

### 3. **Sensors**

- **IMU**: Provides orientation and angular velocity.
- **Odometry**: Ensures accurate vehicle state feedback.
- **3D LiDAR**: Mounted for obstacle detection and environmental scanning.

### 4. **Navigation**

- Integrated with the **Nav2 stack** for autonomous navigation.
- **AMCL (Adaptive Monte Carlo Localization)** for improved positional accuracy.
- **SLAM** techniques implemented for real-time mapping and understanding of the environment.
- Fine-tuned parameters for optimized navigation performance.

### 5. **Manual Control (with external joystick)**

- Added support for joystick-based manual control in the simulation environment, enabling users to test vehicle movement interactively.

### 6. **Visualization**

- Full model and sensor data visualization in **RViz2**, providing insights into robot states and environmental feedback.

## Requirements

- **ROS2 (Humble)**
- **Gazebo Sim Harmonic**
- **RViz2**
- **Nav2**

## Installation and Usage

Run the following commands to set up and launch the simulation:

1. Clone the repository:
    `git clone https://github.com/alitekes1/ros2-ackermann-vehicle-gz-sim-harmonic-nav2 cd ros2-ackermann-vehicle-gz-sim-harmonic-nav2/`
2. Build the project:
    `colcon build && source install/setup.bash`
3. Set environment variables:
    `export GZ_SIM_RESOURCE_PATH=$GZ_SIM_RESOURCE_PATH:/your/path/ros2-ackermann-vehicle-gz-sim-harmonic-nav2/src export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:/your/path/ros2-ackermann-vehicle-gz-sim-harmonic-nav2/src`
4. Launch the simulation:
    `ros2 launch adbhut_bringup adbhut_spawn.launch.py`
5. Launch navigation:
    `ros2 launch adbhut_bringup localization.launch.py `
6. Set initial pose for AMCL.
7. Set goal pose (2D Nav goal)
