---
layout: post
title: "How Robots Move: Inside the World of Actuators and Motion Modeling"
date: 2024-01-15
categories: Design and modeling
---

# How Robots Move: Inside the World of Actuators and Motion Modeling

Actuators are the muscles of robots — the components that enable motion and interaction with the environment. Whether it’s a robotic arm assembling electronics, a humanoid walking, or a drone flying through a warehouse, actuation systems are at the heart of robotic function. In this post, we explore two fundamental actuation technologies: **electric motors** and **hydraulic actuators**, along with the **transmission mechanisms** that link them to joints, and the **modeling techniques** used to simulate and control their behavior.

---

## 1. Electric Motors in Robotics

Electric motors are the most widely used actuators in modern robotics due to their compact size, precision, and ease of control.

### Types of Motors

- **DC Motors**: Known for simplicity and ease of speed control, they are commonly found in wheeled robots and mobile bases.
- **Brushless DC Motors (BLDC)**: These offer high efficiency and longer lifespan. Used in drones, robotic arms, and electric vehicles.
- **Stepper Motors**: Provide discrete step-wise rotation, ideal for applications like 3D printers, pick-and-place arms, and CNC machines.
- **Servo Motors**: Include built-in feedback systems (typically encoders) for precise control of position and speed.

### Advantages
- High precision and responsiveness.
- Easy integration with electronic control systems.
- Widely available and relatively affordable.

### Limitations
- Lower torque density compared to hydraulic systems.
- May require complex gear systems for torque amplification in heavy-load applications.

### Key Suppliers
- [Maxon Group](https://www.maxongroup.com/en-us/market-solutions/mobility-solutions/robotics)
- [Toyo Robotics](https://www.toyorobotics.co/)
- [ElectroCraft](https://www.electrocraft.com/motors-for/robotics/)
- [RobotShop](https://www.robotshop.com/collections/motors-actuators)

---

## 2. Hydraulic Actuation

Hydraulic actuators use pressurized fluids to create mechanical motion. They are favored in systems that require **high force output** in compact spaces.

### How They Work

A hydraulic system typically includes:
- **Pump**: Supplies pressurized fluid.
- **Reservoir**: Stores hydraulic fluid.
- **Control Valves**: Manage pressure and direction.
- **Cylinders or Motors**: Convert fluid power into linear or rotary motion.

### Advantages
- High power-to-weight ratio.
- Smooth, controlled motion under heavy loads.
- Effective in harsh or outdoor environments.

### Limitations
- Requires complex plumbing and sealing.
- Potential for fluid leakage.
- Typically bulkier and heavier than electric systems.

### Use Cases
- Humanoid robots (e.g., Boston Dynamics Atlas)
- Industrial automation with high-load demands
- Robotic exoskeletons and quadrupeds

### Key Suppliers
- [Kyntronics](https://www.kyntronics.com/)
- [York Precision](https://yorkpmh.com/products/custom-hydraulic-actuators/)
- [Tolomatic](https://www.tolomatic.com/)
- [DirectIndustry Listings](https://www.directindustry.com/industrial-manufacturer/hydraulic-actuator-64972.html)

---

## 3. Transmission Mechanisms

Transmissions connect actuators to joints and allow for torque amplification, speed adjustment, and controlled motion.

### Types of Transmissions

#### ⚙️ Gear-Based Transmissions
- **Planetary Gears**: Compact, high-load handling.
- **Harmonic Drives**: Zero-backlash and high precision.
- **Cycloidal Drives**: High torque, low backlash, very durable.

#### 🔗 Belt, Chain, and Cable Drives
- Flexible routing, ideal for lightweight designs.
- Common in collaborative robots and snake robots.

#### 🔩 Compliant Transmissions
- **Series Elastic Actuators (SEAs)**: Add spring elements to absorb impact, ideal for safe interaction.

### Cycloidal Drives Deep Dive
Cycloidal gearboxes offer:
- High torque density.
- Very low backlash.
- Load-sharing across multiple teeth = higher durability.
- Example applications: Denso robots, collaborative arms, legged robots.

### Comparison Table

| Mechanism           | Precision | Backlash | Torque Density | Weight | Maintenance |
|---------------------|-----------|----------|----------------|--------|-------------|
| Harmonic Drive      | High      | Low      | Medium          | Medium | Medium      |
| Planetary Gears     | Medium    | Medium   | Medium          | High   | Low         |
| Cycloidal Drive     | High      | Very Low | High            | High   | Medium      |
| Cable Systems       | Low       | High     | Low             | Low    | High        |

### Key Suppliers
- [Harmonic Drive](https://www.harmonicdrive.net/)
- [Nabtesco](https://www.nabtesco.de/en/technology/cycloidal-gears)
- [Tallman Robotics](https://www.tallman-robotics.com/cycloidal-gears/)
- [HVH Industrial](https://hvhindustrial.com/sub-category/robotics-gear-reducers/18256)

---

## 4. Actuator Modeling for Control and Simulation

Modeling is crucial for:
- Designing efficient controllers (e.g., PID, MPC)
- Realistic simulation in digital environments
- Predicting performance and wear

### a. Electric Motor Models

**Voltage Equation:**  
$$ V = L \frac{di}{dt} + R i + K_e \omega $$

**Torque Output:**  
$$ \tau = K_t \cdot i $$

Where:
- $V$: voltage  
- $i$: current  
- $L$: inductance  
- $R$: resistance  
- $\omega$: angular velocity  
- $K_t$: torque constant  
- $K_e$: back EMF constant

### b. Hydraulic Actuator Models

**Force Equation:**  
$$ F = P \cdot A $$

Where:
- $P$: fluid pressure  
- $A$: piston area

Modeling also includes valve dynamics, fluid compressibility, and leakage losses.

### c. Transmission Modeling

**Gear Ratio:**  
$$ r = \frac{\omega_{motor}}{\omega_{joint}} $$

Include losses: efficiency $\eta$, backlash, friction  
Compliance models: springs and dampers

### d. Compliant Actuator Model

$$ \tau = k \cdot (\theta_{motor} - \theta_{load}) $$

Where $k$ is the spring constant.

### e. Simulation Tools
- **MATLAB/Simulink**: Dynamic modeling and control design.
- **Gazebo / ROS 2 Ignition**: Robotics simulation with physical modeling.
- **NVIDIA Isaac Sim**: Photorealistic physics simulations for AI-powered robots.

---

## 5. Electric vs Hydraulic — Summary

| Feature             | Electric Motors        | Hydraulic Actuators        |
|---------------------|------------------------|-----------------------------|
| Power Density        | Medium                 | High                        |
| Precision & Control  | High                   | Moderate                    |
| Maintenance          | Low                    | High                        |
| Speed                | Fast                   | Slower                      |
| Use Case             | Precision arms, drones | Heavy-load or dynamic legs  |

---

## 6. Conclusion

Selecting the right actuator and transmission system is essential to robotic performance, efficiency, and safety. Electric motors offer precision and control, while hydraulic actuators bring raw power for demanding tasks. Transmission design — from harmonic to cycloidal — bridges the gap between actuator capabilities and robotic function.

By accurately modeling actuators, roboticists can develop sophisticated control strategies and simulations that save time, reduce cost, and increase reliability.

---

## 🔗 References & Further Reading
- Spong, Hutchinson, Vidyasagar. *Robot Modeling and Control*
- [Maxon Motor Robotics Applications](https://www.maxongroup.com/en-us/market-solutions/mobility-solutions/robotics)
- [Harmonic Drive Systems](https://www.harmonicdrive.net/)
- [Boston Dynamics - Hydraulic Actuation](https://www.bostondynamics.com/)
- [MATLAB Simscape for Robotics](https://www.mathworks.com/products/simscape.html)
- [NVIDIA Isaac Sim](https://developer.nvidia.com/isaac-sim)

---

*Next Topic: Sensor Fusion in Robotics — Combining LiDAR, IMU, Vision, and More*

