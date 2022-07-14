project still is in progress (just write the URDF file and make a launch file)

plan: make an autonomous robot able to navigate in dynamic unknown environment able to control remotely

Hardware : 
	Differential robot with one caster wheel:
1. onboard computer : raspberry pi “Ubuntu and ROS2 installed”
2. Arduino controller
3. DC motors + drivers
4. 3 ultrasound sensor
5. camera
6. scanner laser (optional) a little expensive but make job easier:)

Software: 
ROS2 ,  C++, Python,  

simulator:
Gazebo, Rviz

Run this project till now:

you should have Ubuntu, ros2 , gazebo, colcon installed

1- download the file and Extract to your “work_space/src”(make a folder with any name with sub-folder src) 
‘’’’’’’’’’’’’’’important change the file name to my_robot

2- open a terminal move to your work_space folder: 
aidin@aidin-HP-Pavilion-dv7-Notebook-PC:~/Desktop/ww$    “in my case”

3- build the project:  
$ colcon build

4- source the file:
$ source install/setup.bash

5- run launch file:
$ ros2 launch my_robot sim.launch.py
or
$ ros2 launch my_robot sim.launch.py world:=./src/my_robot/world.world

you can control the robot with teleop_node with joy or keyboard …
for example open a new terminal and run this command:
$ ros2 run teleop_twist_keyboard teleop_twist_keyboard # my_robot

