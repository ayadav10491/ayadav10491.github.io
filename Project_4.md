---
layout: project
title: Multi-Robot Formation Control
---

# Multi-Robot Formation Control

---
## Objective
---
<p align="justify">
The project focuses on decentralized formation control of multi-robot systems using graph theory and consensus algorithms. The goal is to coordinate multiple autonomous mobile robots to maintain a desired geometric formation while navigating in an environment.
</p>

---
## Approach
---

### Graph Theory Based Control
<p align="justify">
The formation control problem is modeled using graph theory, where robots are represented as nodes and communication links as edges. The graph structure defines the interaction topology among robots, enabling distributed coordination without centralized control.
</p>

### Controller Architecture
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/controller_mbse.png?raw=true" width="600" height="400">
<p align="center" style="font-size:12px">Model-Based Systems Engineering (MBSE) Controller Architecture</p>

### Communication Graph
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/graph.png?raw=true" width="600" height="400">
<p align="center" style="font-size:12px">Graph representation of robot communication topology</p>

---
## Implementation
---

### Robot Model
- **Type**: Unicycle mobile robots
- **Number of Agents**: 4 robots
- **Control Approach**: Decentralized consensus-based control
- **Platform**: MATLAB/Simulink

### Consensus Algorithm
<p align="justify">
The consensus algorithm ensures that all robots agree on a common reference while maintaining relative positions. Each robot computes its control input based on information from its neighboring robots according to the communication graph.
</p>

### Key Features
<ul>
<li><b>Decentralized Control</b>: Each robot makes decisions based on local information from neighbors</li>
<li><b>Formation Maintenance</b>: Robots maintain desired geometric formation during motion</li>
<li><b>Scalability</b>: Graph-based approach allows easy extension to more robots</li>
<li><b>Robustness</b>: Formation persists even with limited communication links</li>
</ul>

---
## Results
---

### Simulation
<p align="justify">
The formation control algorithm was successfully implemented and tested in MATLAB. The simulation demonstrates coordinated motion of four unicycle robots maintaining a predefined formation pattern.
</p>

### Technical Details
<b>Control Law</b>: Consensus-based distributed control<br>
<b>Robot Dynamics</b>: Unicycle kinematic model<br>
<b>Communication</b>: Graph-based topology<br>
<b>Tools</b>: MATLAB, Simulink, Graph Theory<br>

---
## Documentation
---
For detailed theoretical background and implementation details, please refer to the [project report](https://github.com/ayadav10491/Portfolio/blob/master/pdf/MBSE_Formation_Control.pdf).
