## Behaviour based Control Strategy for Double Ackermann Steering Control of Autonomous Tandem Road Rollers

<b><i>v</i></b>


### Objective

<p align="justify">
The project work is an attempt to explore the autonomous capabilities of tandem rollers in the road construction. The project specifically focuses on analyzing the dynamics and
kinematics of tandem rollers, understanding the previously developed work on autonomous navigation including different levels of controls based on perception; later, extending
the same to the edge compaction module of the navigation system. The manual edge compaction for a roller is a complicated task which requires a skilled driver to drive through the edge with the front edge cutter and keeping the rear wheels away from the edge. The autonomous edge controller is an attempt to remove the driver involvement with the automated crab walk application in the roller.  </p>

### Workflow

<ul>
<li> Analysis of Behaviour based Control Strategy </li>
<li> Study of control architecture and communication protocol </li>
<li> Road representation </li>
<li> Edge extraction </li>
<li> Trajectory creation </li>
<li> Crab angle calculation </li>
<li> Trajectory tracking with crab behaviour activated </li>
<li> Edge Cutter activation </li>
<li> Simulation using Unreal Engine and Finroc (ROS inspired tool) </li>
</ul>

### Methodology

#### Integrated Behaviour based Control Strategy 

[Proetzsch 10] proposed a behaviour based control architecture iB2C for the development of complex robotic systems. “It is shown how architectural principles support several behaviour based mechanisms, e. g. coordination mechanisms, behaviour interaction, and hierarchical abstraction”.

<ul>
  <li> <b> Structure and Components </b> </li>
  
  The iB2C behaviour module (B) consists of six signals coming in and out namely, Stimulation s, Inhibition vector <i>i </i>, Input vector <i>e &#8407;</i>, Output vector ~u, Activation vector ~a and Target rating r. The stimulation s is responsible for a gradual initiation of behaviour, while the inhibition vector~i gradually disables it. The combined interaction of s [0, 1] and ~i [0, 1] triggers an activation  signal which sets the limiting value for the influence of behaviour.
  
  <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/ib2c_structure_.JPG?raw=true" width="500" height="180"> 
  
<li> <b> Behaviour Fusion </b> </li>
  <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/fusion.png?raw=true"> 
  
  Behaviour fusion can be achieved using following techniques: 
  <dl>
       <dd>- <b> Maximum Fusion </b> </dd>
       <dd>- <b> Weighted Average Fusion </b> </dd>
  </dl>
</ul>

<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/robot_unreal.gif?raw=true" width="300" height="200"> <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/robot_finroc.gif?raw=true"  width="300" height="200"/>
