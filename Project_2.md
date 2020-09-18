## Behaviour based Control Strategy for Double Ackermann Steering Control of Autonomous Tandem Road Rollers



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
  
  The iB2C behaviour module (B) consists of six signals coming in and out namely, Stimulation <b><i>s </i> </b>, Inhibition vector <b><i>i </i> </b>, Input vector <b> <i>e</i>&#8407;</b>, Output vector <b> <i>u</i>&#8407;</b>, Activation vector <b> <i>a</i>&#8407;</b> and Target rating <b><i>r </i> </b>. The stimulation <b><i>s </i> </b> is responsible for a gradual initiation of behaviour, while the inhibition vector <b> <i>i</i>&#8407;</b> gradually disables it. The combined interaction of <b><i>s </i> </b> [0, 1] and <b> <i>i</i>&#8407;</b> [0, 1] triggers an activation <b><i>l </i> </b> signal which sets the limiting value for the influence of behaviour.
  
  <p align="center"> <b><i>l </i> </b> = <b><i>s </i> </b> (1 - <b><i>i </i> </b>) </p>
  
 The activation signal ( <b><i>l </i> </b> ), further helps in defining a transfer function <b><i>F</i></b> ( <b> <i>e</i>&#8407;</b>,  <b><i>l </i> </b> ) which later defines the respective output vector <b> <i>u</i>&#8407;</b> of the system i.e. F </i></b> ( <b> <i>e</i>&#8407;</b>,  <b><i>l </i> </b> ) = <b> <i>u</i>&#8407;</b>. The data from sensors, (e.g. distance measurements, acceleration) also forms an input vector <b> <i> e &#8712; R<sub>m </sub> </i> </b>. The activation <b> <i>l</i></b> also limits the activity <b> <i>a </i></b>  of the behaviour <b> <i>B</i></b>, such that <b> <i>l&#8804; a </i></b> . Behaviour  <b> <i>B</i></b> can thus be described as:
<p align="center">  <b><i>B</i></b> = (<b><i> f<sub>a </sub>, f<sub>r</sub>, F </b></i>)  </p> 
  
where, <b><i> f<sub>a </sub> </b></i> is the activity function,  <b><i> f<sub>r</sub> </b></i> is the target rating function,  <b><i> F</b></i> is the transfer function
of the behaviour. It is interesting to note that, like the transfer function, activation function  <b><i> f<sub>a </sub> </b></i> is a function of <b> <i>e</i>&#8407;</b> and <b><i>l </i> </b> ; and also defines activity signal <b><i>a</i> </b>  and activity vector <b> <i>a</i>&#8407;</b> .
  
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
