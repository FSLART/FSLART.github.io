# Autonomous Driving Technical Documentation

## System dependencies

These are the dependencies you need to install beforehand in the operating system:

- ROS Humble
- PyTorch
- LibTorch

or

- Docker

## Building and running

### Bare metal

- First, you need to setup a ROS workspace. To do that, create a new folder with a `src` directory inside. This can be for example `mkdir -p /home/myusername/ros2_ws/src`.

- Place the following repositories in the `src` subdirectory:
    - [lart_msgs](https://github.com/FSLART/lart_msgs): Common team-defined ROS messages.
    - [local_mapper](https://github.com/FSLART/local_mapping_ros): Local mapping (cone detection and back-projection).
    - [planner](https://github.com/FSLART/ft-fsd-path-planning): Path planning
    - [Spac](https://github.com/FSLART/Spac): Pure pursuit PID controller

- Install workspace dependencies running `rosdep install -i -y --from-path src` from the `ros2_ws` directory.

- Build the workspace running `colcon build --symlink-install`.

- Source the installation script `source install/setup.bash`.

- Start each node as stated in the documentation of each repository.

### Docker

- Work in progress...