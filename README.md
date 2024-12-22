# Homework1

- Clone the repo:

$ git clone https://github.com/Pixel-0-1/Homework1.git


- Build the new package:

$ colcon build


- Source the setup files:

$ source install/setup.bash


- Launch Rviz with:

$ ros2 launch arm_description display.launch.py


- Launch Gazebo with:

$ ros2 launch arm_gazebo arm_gazebo.launch.py


- Connect to the container from another terminal:

$ ./docker_connect.sh 


Once the terminal is connected is possible :

- start arm_controller_node, in order to observe the current position of the robot or the points through which it passes before reaching a position, with:

$ ros2 run arm_control arm_controller_node


- bring up the camera, to observe what is along a specific trajectory of the robot, with:

$ ros2 run rqt_image_view  rqt_image_view


- force the robot to reach a position with:

$ ros2 topic pub --once /position_controller/commands std_msgs/msg/Float64MultiArray "data: [0.5,-0.3,0.8,0.2]"

