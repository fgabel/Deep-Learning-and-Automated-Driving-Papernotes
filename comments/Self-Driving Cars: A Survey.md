# [Self-Driving Cars: A Survey](https://arxiv.org/pdf/1901.04407.pdf)

**TLDR: A general overview of self-driving car architecture (often perception and decision-making) and subdivided system components.

* A typical Architecture of a self-Driving car in the following Figure. The different subsystems are described below.  
![Self-driving car architecture](../images/self-driving-car-architecture.png)

* The **perception** module consists of all sensors - LiDAR, RaDAR, cameras, IMUs, GNSS/RTK, odometers etc., the **decision making** module is responsible for navigating the car
from its initial position to the final goal defined by the user, considering the current car's State and the internal representation of the environment, as
well as traffic rules and passengers' safety and comfort. The **Localizer subsystem** (Figure 1) is responsible
for estimating the car's State (pose, linear velocities, angular velocities, etc.) in relation to static maps of the environment. These static maps, or **Offline Maps**, are
computed automatically before the autonomous operation, typically using the sensors of the self-driving car itself, although
manual annotations (i.e., the position of pedestrian crosswalks
or of traffic lights) or editions (for removing non-static objects
captured by the sensors) are usually required. A self-driving car may use more modi of offline maps, such as occupancy grid maps, remission maps or landmark maps.
The **Mapper** subsystem receives as input the Offline Maps
and the self-driving car's State, and generates as output the online map. This online map is typically a merge of information
present in the Offline Maps and an occupancy grid map computed online using sensors’ data and the current car's State. 
