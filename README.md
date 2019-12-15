[![Python 2.7](https://img.shields.io/badge/python-2.7-blue.svg)](https://www.python.org/downloads/release/python-270/)
[![Python 3.6](https://img.shields.io/badge/python-3.6-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![ROS Distro: Kinetic](https://img.shields.io/badge/ROS-Kinetic-green.svg)](http://wiki.ros.org/kinetic)
[![License: BSD](https://img.shields.io/badge/License-BSD-yellow.svg)](./LICENSE)

<br/>
<img src="docs/logo.png?raw=true" width="300">

# Collision Avoidance System
Collision Avoidance System for Self-Driving Vehicles by Delta Autonomy, Robotics Institute, CMU. This stack was developed for my MRSD capstone project. 

<img src="docs/collision-avoidance.png?raw=true" width="250">

## Description

Our use-case involves an oncoming vehicle encroaching into the ego-vehicle's (heavy-duty truck) lane, on a two-lane countryside highway. The perception algorithms perform the detection and tracking of vehicles, and lane marking detection, using a sensor fusion of a monocular camera and RADAR. The prediction algorithms predict the trajectories of all vehicles in the environment including the ego-vehicle. Based on the predicted trajectories, the probability of collision, position and time-to-impact is computed. An evasive maneuver, such as steering or braking, is planned and executed to avoid or mitigate the crash. The project was developed in Carla simulator and ROS.

## Results
- Collisions detected in 90% cases with 80% accuracy, and mitigated in 60% cases via an evasive maneuver or braking strategy.
- Achieved mAP of 0.7-0.9 for object detection, lane detection with offsets less than 0.5m.
- Our tracking and sensor fusion pipeline achieved MOTA 75% and MOTP 85%.
- Prediction of trajectories of oncoming vehicles within an RMSE of 2m, and ego-vehicle within an RMSE of 1m, 2-3 seconds in future.
- The entire pipeline runs at 21-24 FPS along with a NVIDIA Titan V GPU.
- We also developed custom maps in RoadRunner and created collision scenarios in Carla.
- Developed a JavaScript based dashboard GUI interfaced with ROS in real-time.

## Issues and Contributions
This repository is only a collection of all the ROS packages developed by us. Feel free to raise issues and pull requests on the original repositories.

---

My primary contributions were in developing the Perception, Tracking/Fusion Pipelines and the stack for the RC Car Platform, along with managing the software stack and developing DeltaViz, which a JavaScript based GUI for ROS. My secondary contributions also include developing a custom RADAR sensor in Carla ROS Bridge. Find out more about our project on [deltaautonomy.github.io](http://deltaautonomy.github.io/). This stack was also developed by [@ykarmesh](https://github.com/ykarmesh), [@singaporv](https://github.com/singaporv) and [@pparmesh](https://github.com/pparmesh).

### DeltaViz

![DeltaViz](docs/deltaviz.jpg?raw=true "DeltaViz")

## Sensor Fusion, Tracking, and Prediction

![Tracking Fusion](docs/tracking-fusion.jpg?raw=true "Tracking Fusion")
![Prediction](docs/traj-pred.PNG?raw=true "Prediction")

### RC Car Platform

![RC Car](docs/rccardiag.jpg?raw=true "RC Car")
![RC Car Camera RADAR Sensor Fusion](docs/rccardet.jpg?raw=true "Camera RADAR Sensor Fusion")
