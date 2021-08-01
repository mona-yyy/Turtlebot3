# Turtlebot3:
Use Turtlebot3 with SLAM approach to create and save a map firstly, install Ubuntu on PC and open the terminal and install ROS 1 on Remote PC using commands like a video in the below:

![0FA6DE8F-6793-48D9-BB66-B90D13186482_1_102_o](https://user-images.githubusercontent.com/85816257/127595441-3a2aef63-a5eb-4120-95ff-34c747e39752.jpeg)

# Install TurtleBot3 Packages:
Then Install TurtleBot3 via Debian Packages by this commands :

$ sudo apt-get install ros-melodic-dynamixel-sdk

$ sudo apt-get install ros-melodic-turtlebot3-msgs

$ sudo apt-get install ros-melodic-turtlebot3

![31698A9D-D78F-4D47-ADE5-A22CE8785572_1_102_o](https://user-images.githubusercontent.com/85816257/127595947-be9bf514-1329-4acc-8bd2-4f2ad9e6e1b5.jpeg)

# Set TurtleBot3 Model Name:

i Use this commands to do it :

$ echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc

$ echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc

To Connect PC to a WiFi device and find the assigned IP address i used this command :

$ ifconfig

To Source the bashrc with below command use this command :

$ source ~/.bashrc


![p3](https://user-images.githubusercontent.com/85816257/127596235-0df54b72-664d-4419-951e-5443bca5a991.png)

# Gazebo Simulation:

You need to Install Simulation Packages by using commands in the below :

$ cd ~/catkin_ws/src/

$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

$ cd ~/catkin_ws

$ catkin_make

![536A8DB2-F76A-46AD-9660-3ED1ECF225C2_1_102_o](https://user-images.githubusercontent.com/85816257/127597039-021bf5d8-f03d-40d4-82b0-f81de1a56144.jpeg)

# Launch Simulation World:

1-Empty World:
You need using commands like a video in the below:

![B35A9265-4F09-462D-B65F-6CE8CC536062_1_102_o](https://user-images.githubusercontent.com/85816257/127597542-1b7d19ef-4e1a-4937-aed0-0479adccb255.jpeg)

2-TurtleBot3 World:

Using this commands:

$ export TURTLEBOT3_MODEL=waffle

$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

![p6](https://user-images.githubusercontent.com/85816257/127598260-b4ccc369-3ba3-4e4e-a028-5adcdde3c5d5.png)

3-TurtleBot3 House:

Using this commands:

$ export TURTLEBOT3_MODEL=waffle_pi

$ roslaunch turtlebot3_gazebo turtlebot3_house.launch

![p7](https://user-images.githubusercontent.com/85816257/127599566-a3f64cd4-4a50-4b47-be4a-880bebef0326.png)

Then use this command to operate TurtleBot3 :

($ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch) 

# SLAM Simulation:

When SLAM in Gazebo simulator, you can select or create various environments and robot models in virtual world .

# Launch Simulation World:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

# Run SLAM Node:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

# Run Teleoperation Node:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

![p8](https://user-images.githubusercontent.com/85816257/127771574-1608ed14-33c4-4389-9a7f-76ed9e51c87b.png)
![p9](https://user-images.githubusercontent.com/85816257/127771580-5f135ded-13cf-46ef-b95a-597ebdbb126c.png)

Then move the robot by using (a,s,w,d,x) to complete all the map

# Save Map:

![Screen Shot 2021-08-01 at 5 37 41 PM](https://user-images.githubusercontent.com/85816257/127774916-2024bcc5-9e81-4ca8-ba87-a37f757cf6d1.png)

Then use this command ($ rosrun map_server map_saver -f ~/map )

![Screen Shot 2021-08-01 at 5 41 07 PM](https://user-images.githubusercontent.com/85816257/127774992-fcc8a773-2c89-430d-825a-16abb981ef37.png)

