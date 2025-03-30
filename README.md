# ROS 2 TurtleBot Perception Project

## Prerequisites

Ensure you have the following dependencies installed:

- ROS 2 Humble
- Python 3
- OpenCV
- PyTorch
- Torch
- Numpy
- Time
- Os

## Installation

### 1. Cloning the Repository

Start by cloning the project repository and setting up the workspace:

```bash
mkdir -p ros_perception_ws/src
cd ~/ros_perception_ws/src

git clone https://github.com/ChandhanSaai/ROS_2_TurtleBot_perception_project.git

cd ~/ros_perception_ws

# Build and install the package
export TURTLEBOT3_MODEL=waffle
source /opt/ros/humble/setup.bash
colcon build --symlink-install
```

### 2. Launching the Gazebo Simulation

Run the following commands to start the Gazebo world:

```bash
source install/setup.bash
source /usr/share/gazebo/setup.bash  # This step may not be necessary
ros2 launch enpm673_final_proj enpm673_world.launch.py "verbose:=true"
```

### 3. Running the Python Node

Open a new terminal and execute the command below to launch the perception node:

```bash
cd ~/ros_perception_ws
export TURTLEBOT3_MODEL=waffle

source install/setup.bash
ros2 run enpm673_final_proj enpm673_final_proj_main.py
```

## Output

### Gazebo Simulation

![Gazebo](Gazebo_implementation_gif.gif)

### Real-World Implementation

![Real_world](Real_world_implementation_gif.gif)

### Stop Sign Detection

![Stop sign](Stop_sign_picture.jpg)

### Horizon Line Detection

![Horizon line](horizon_line_image.png)

### Optical Flow

![Optical flow](Optical_flow_picture.jpg)

## System Flow Diagram

![System flow](System_flow_picture.png)

