# Autonomous Navigation and Platform Landing
The goal of this project is to further advancements in autonomous navigation and platform landing. Using ROS, I programmed robotic hardware and software. The ROS distribution used was melodic along with Ubuntu 18.04. Additionally, I used a UGV, UAV, and a Motion Capture system.                                                                                               


## Hardware Used
This project used a variety of hardware and robotic accessories: 
- Host Ubuntu PC
- Vicon Motion Capture System
- Clearpath Robotics Jackal UGV
- UAV
- Point Grey Bumbleebee2 Stereo Vision Camera
- Hokuyo UST-10LX 2D LiDAR Sensor


## Vicon 

Vicon, a motion capture system, was utilized at the beginning of this project to learn position and localization. It provided the location of the Jackal UGV and UAV within the specified environment. 

### Camera Calibration 
To use the Vicon Motion Capture system, camera calibration is required. A wand provided for the system has flashing red LEDs. You must then walk around and wave it until the cameras no longer blink. You then must place the wand flat on the ground to set the origin of the environment.

![IMG_8652](https://user-images.githubusercontent.com/98404383/180620554-91ecd706-19f4-41d0-904d-86bfed7c094c.jpeg)


### Object Identification 
Object identification is essential to provide an interaction between the Vicon system, Jackal UGV, and UAV. The Jackal and UAV both had reflective markers on top for the Vicon system to recognize and locate them in the environment. Within the Vicon Tracker software, you select them being seen by the camera and  create new objects with their names assigned. This allows for the location data to communicate when you launch scripts.  


![IMG_8648](https://user-images.githubusercontent.com/98404383/180620686-0ae67176-34ef-4a5e-9fc4-4a7e92de694d.JPG)


### Scripts
For behavioral control of the UGV and UAV, Python, and ROS are used for programming implementations. The Jackal UGV and UAV both had ROS topics of the Vicon Motion Capture system. This was done with the usage of ROS launch files. Once the location communication was set, I created and wrote several programs for different trajectories for the Vicon environment. Each program application provided a scenario for the UAV to land on the platform while in motion. 



https://user-images.githubusercontent.com/98404383/180629362-b7529f71-5982-4102-8732-fd885f3d8a86.mp4




## Using Jackal UGV for Autonomous Navigation 
To further advance with autonomous navigation, I began working with the Jackal UGV individually. The Vicon Motion Capture System allowed an understanding of the localization of objects; however, it was within a set environment. 


### Simulation
Before working with the physical Jackal, I created a simulation using Gazebo and Rviz on the host PC using ROS Melodic. Using Gazebo alongside RViz, I generated a unique map of the simulated room using the configuration of lidar sensors on a Jackal UGV. Utilizing multiple ROS tools, which included Navigation Stack, SLAM, Gmapping, Localization, and Visualization the map served as a guide for the testing and validation. 


<img width="1622" alt="Screen Shot 2022-07-06 at 6 40 35 PM" src="https://user-images.githubusercontent.com/98404383/180628936-ef11a5c6-ed48-4cbc-bbfe-c99b213a7054.png">


### Hardware
The Jackal UGV used has an onboard computer that is fully integrated with ROS. Before working with physical Jackal’s accessories, I determine it was useful to completely reset the Jackal’s OS. By setting everything to default, I was able to make it as configurable as I wanted. After these resetting changes, I connected a PS4 controller to manually control the Jackal and successfully confirmed everything was installed correctly in conjunction with the default robot configurations. 


![IMG_8574](https://user-images.githubusercontent.com/98404383/180629410-eeb4ef37-c50d-4bf4-a994-60cd93fb1679.png)


After confirming proper functionality, I added additional Accessories. This included a Point Grey Bumblebee2 and a Hokuyo UST-10LX. The Bumbleebee2 is a Stereo Vision Camera and the UST-10LX is a 2D LiDAR. After the proper network configuration of the host PC and Jackal, I was able to source the Jackal UGV to reflect its activity onto the PC. 


https://user-images.githubusercontent.com/98404383/180629384-1bc176bd-ec11-4c7b-8740-de0aecf23989.mp4

