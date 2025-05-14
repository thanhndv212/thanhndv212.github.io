---
layout: post
title: "Everything you need to build and play with the open-source 3D printed manipulator SO-ARM from LeRobot"
date: 2025-05-14
categories: SO-ARM
---
After many years of studyiing and working in Robotics, I still find it unclear **how** to do a proper robotic project (The question "**Why**" will be left out to you.).
Since working with physical robots means that you need to know a bit of everything in engineering, it somehow creates a barrier to new-comers with a lot of confusion:
 ```from choosing/building hardwares (body material, actuators, sensors) -> working in simulation (yes we all want to imagine how it moves first before it actually moves) -> building applications (eventually a robot should be able to do something helpful or funny) -> transfering to real hardwares (now the real work only begins)-> debuging/maintaining performance -> etc.``` Therefore, I will gather all public resources combining with my undestanding and experience to organize this little project first for me to see how far I have gone in robotics and secodn for anyone who comes to robotics and is interested to understand a complete framework of a robotics projects. This blog will cover my progress and will be updated occasionally.
 
The tentative content I want to cover is below.

---

## Content Outline

1. [What is the purpose of this robot?](#1-electric-motors-in-robotics)  
2. [Hardware selection](#2-hydraulic-actuation)
   - 3D design/printing
   - Motors
   - Sensors
   - Hardware assembling
   - Calibration with Figaroh+
3. [Modeling](#3-transmission-mechanisms)  
   - From 3D design to physics simulated model
   - Creating a scene (where the robot interacts with environment)
4. [ROS2 integration](#4-actuator-modeling-for-control-and-simulation)
   - URDF
   - MoveIt setup assistant
   - ROS2 control
5. [Simulation](#5-electric-vs-hydraulic--summary)
   - MoveIt + Rviz2
   - Gazebo
   - Mujoco
   - IsaacSim
6. [Control and Learning](#6-conclusion)
   - Feetech motor control
      - Hardware interace with ROS2
      - Feetech sdk with python
   - Motion planning
   - Immitation Learning with Diffusion Policy by LeRobot
   - Reinforcement Learning
      - With IsaacLab (required NVIDIA GPU)
      - With Mujoco + SB3
7. [Experiments](#-references--further-reading)
8. [Tips and tricks]()
---

(To be updated)

---
