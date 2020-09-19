# Behaviour based Control Strategy for Double Ackermann Steering Control of Autonomous Tandem Road Rollers



## Objective

<p align="justify">
The project work is an attempt to explore the autonomous capabilities of tandem rollers in the road construction. The project specifically focuses on analyzing the dynamics and
kinematics of tandem rollers, understanding the previously developed work on autonomous navigation including different levels of controls based on perception; later, extending
the same to the edge compaction module of the navigation system. The manual edge compaction for a roller is a complicated task which requires a skilled driver to drive through the edge with the front edge cutter and keeping the rear wheels away from the edge. The autonomous edge controller is an attempt to remove the driver involvement with the automated crab walk application in the roller.  </p>

## Workflow

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

## Backgroud

### Integrated Behaviour based Control Strategy (iB2C)

[Proetzsch 10] proposed a behaviour based control architecture iB2C for the development of complex robotic systems. “It is shown how architectural principles support several behaviour based mechanisms, e. g. coordination mechanisms, behaviour interaction, and hierarchical abstraction”.

<ul>
  <li> <b> Structure and Components </b> </li>
  <p align="justify">
  The iB2C behaviour module (B) consists of six signals coming in and out namely, Stimulation <b><i>s </i> </b>, Inhibition vector <b><i>i </i> </b>, Input vector <b> <i>e</i>&#8407;</b>, Output vector <b> <i>u</i>&#8407;</b>, Activation vector <b> <i>a</i>&#8407;</b> and Target rating <b><i>r </i> </b>. The stimulation <b><i>s </i> </b> is responsible for a gradual initiation of behaviour, while the inhibition vector <b> <i>i</i>&#8407;</b> gradually disables it. The combined interaction of <b><i>s </i> </b> [0, 1] and <b> <i>i</i>&#8407;</b> [0, 1] triggers an activation <b><i>l </i> </b> signal which sets the limiting value for the influence of behaviour. </p>
  
  <p align="center"> <b><i>l </i> </b> = <b><i>s </i> </b> (1 - <b><i>i </i> </b>) </p>
  
 <p align="justify"> The activation signal ( <b><i>l </i> </b> ), further helps in defining a transfer function <b><i>F</i></b> ( <b> <i>e</i>&#8407;</b>,  <b><i>l </i> </b> ) which later defines the respective output vector <b> <i>u</i>&#8407;</b> of the system i.e. F </i></b> ( <b> <i>e</i>&#8407;</b>,  <b><i>l </i> </b> ) = <b> <i>u</i>&#8407;</b>. The data from sensors, (e.g. distance measurements, acceleration) also forms an input vector <b> <i> e &#8712; R<sub>m </sub> </i> </b>. The activation <b> <i>l</i></b> also limits the activity <b> <i>a </i></b>  of the behaviour <b> <i>B</i></b>, such that <b> <i>l&#8804; a </i></b> . Behaviour  <b> <i>B</i></b> can thus be described as:</p>
<p align="center">  <b><i>B</i></b> = (<b><i> f<sub>a </sub> , f<sub>r</sub> , F </b></i>)  </p> 
 
<p align="justify">
where, <b><i> f<sub>a </sub> </b></i> is the activity function,  <b><i> f<sub>r</sub> </b></i> is the target rating function,  <b><i> F</b></i> is the transfer function
of the behaviour. It is interesting to note that, like the transfer function, activation function  <b><i> f<sub>a </sub> </b></i> is a function of <b> <i>e</i>&#8407;</b> and <b><i>l </i> </b> ; and also defines activity signal <b><i>a</i> </b>  and activity vector <b> <i>a</i>&#8407;</b> . </p>
  
  <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/ib2c_structure_.JPG?raw=true"> 
 <p align="center" style="font-size:12px"> The basic design of iB2C Behavior and Percept module  </p> 
  
<li> <b> Behaviour Fusion </b> </li>

  <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/fusion.png?raw=true"> 
  <p align="center" style="font-size:12px"> Behaviour group containing iB2C modules and iB2C fusion modules  </p> 

  Behaviour fusion can be achieved using following techniques: 
  <dl>
  <dd>- <b> <i> Maximum Fusion </i> </b> </dd>
  <dd>- <b> <i> Weighted Average Fusion </i> </b> </dd>
  </dl>
</ul>
<br>

### Control Architecture Integrating Different Level Of Navigation Tasks 

<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/architecture - Copy.png?raw=true" >
<p align="center" style="font-size:12px"> REACTiON control architecture with Remote Interface [Wolf 18][Ropertz 18b] </p>  <br>

### Remote Interface based on 5G AMMCOA (Autonomous Mobile Machine Communication for Off-Road Applications) Protocol
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/ammacoa.png?raw=true" > <br>

## Related Work 

### Road Representation and Edge Extraction
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/road_representation.png?raw=true" >
<p align="center" style="font-size:12px"> Road R representation with Seam <b> <i>S</i>&#8407;</b> , Lane <b> <i>L</i>&#8407;</b>, Edge <b> <i>E</i>&#8407;</b>, Grid <b> <i>G</i>&#8407;</b> and Tracks <b> <i>T</i>&#8407;</b> [Wolf 19] </p>  <br>

### Bicycle Model
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/bicycle_model.png?raw=true" > <br>


## Concept and Implementation

<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/methodolgy.png?raw=true" >
<p align="center" style="font-size:12px"> Schematic representation of the approach</p> 

### Edge Compaction Behaviour 
<p><img src="https://github.com/ayadav10491/Portfolio/blob/master/images/implementation_edge_compaction_behaviour - Copy.png?raw=true" > </p>

### Trajectory Decision based on Behaviour Fusion
<p><img src="https://github.com/ayadav10491/Portfolio/blob/master/images/task_trajectory.png?raw=true" > <br> </p>

### Trajectory Tracking 

<ul>
  <li>  <b>Pilot </b>
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/pilot.png?raw=true" >
<p align="center" style="font-size:12px"> Pilot decides the maneuvering parameters</p> 
</li>
  
<li>  <b>Steering Controller </b>

<p>Receives the maneuvering parameters from the Pilot and transforms them into wheel angles and velocity </p> <br>
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/controller.png?raw=true" >
<p align="center" style="font-size:12px">Controller input to ackermann steering hardware</p>  <br>
</li>

</ul>

## Results

### Simulation on Unreal Engine
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/robot_unreal.gif?raw=true" width="500" height="250"> <br>

### Simulation on FinGUi
<img src="https://github.com/ayadav10491/Portfolio/blob/master/images/robot_finroc.gif?raw=true"  width="500" height="250"/><br>
