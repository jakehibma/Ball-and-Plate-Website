# Ball-on-Plate
-----------------------------------------------------------------------------------------
## 1. Introduction
The 2 DOF Ball Balancer or Project 2 is a system that will recognize the ball's motion on the plate and adjust its orientation to ensure that the ball is in control. MATLAB/Simulink will use a PD based control with multiple loops to control the system which will then be tested in CoppeliaSim. The system is a vision based control experiment that will communicate the balls position and two rotary servo motors will act on this to ensure that the ball will not fall off the plate.
### 1.1 Objectives
1. Create a mathematical model of the system using MATLAB/Simulink
2. Design a proportional-derivative control that will balance the ball on the plate
3. Simulate the MATLAB/Simulink control in CoppeliaSim to prove our PD control works 
4. Build a web page on GitHub that explains how the system works
### 1.2 Equipment
- 2 DOF Ball Balancer made by Quanser
- MATLAB/Simulink
- CoppeliaSim
- GitHub

## 2. Modeling
### 2.1 Background
<p align='center'>
  <img src="Images/ball.jpg">
  Figure 1. One Dimensional View of the Free Body Diagram
  </p>
Figure 1 shows the one dimensional view of the FBD of the ball and plate design. It includes a rotary servo motor that adjusts the plate to keep the ball on. The ball is allowed to move freely and the purpose of this program is to adjust and maintain stability. 

### 2.2 Nonlinear Equation of Motion
Force due to gravity: 

<p align='center'>
  <img src="Equations/Equation 1.gif">
  </p>

Force cause by ball rotation:  
<p align='center'>
  <img src="Equations/Equations 2.png">
  </p>

Where, 
<p align='center'>
  <img src="Equations/Equation 3.png">
  </p>

Force on ball in x-direction: 
<p align='center'>
  <img src="Equations/Equation 4.png">
  </p>


Non-linear equation of motion: 
<p align='center'>
  <img src="Equations/Equation 5.png">
  </p>

Acceleration of the ball:
<p align='center'>
  <img src="Equations/Equation 6.png">
  </p>
  
### 2.3 Relative Servo 
Relate motor angle to beam angle: 
<p align='center'>
  <img src="Equations/Equation 7.png">
  </p>

Take sine of motor shaft: 
<p align='center'>
  <img src="Equations/Equation 8.png">
  </p>

Equation of motion relating motor to ball: 
<p align='center'>
  <img src="Equations/Equation 9.png">
  </p>

Approximation that <img src="Equations/Equation 11.png"> yields linearized equation of motion:

<p align='center'>
  <img src="Equations/equation 10.png">
  </p>

<p align='center'>
  <img src="Images/table.GIF">
  </p>

<p align='center'>
  Table 1. Describes the Variables Seen in the Equations Above.
  </p>

## 3. Sensor Calibration
### 3.1 Background

<p align='center'>
  <img src="Images/Physical System.png">
  Figure #:
  </p>
  
<p align='center'>
  <img src="Images/Coppelia Model.png">
  Figure #:
  </p>
            
### 3.2 Camera Vision
<p align='center'>
  <img src="Images/Coordinate System.png">
  Figure #: Position of the Ball on the Plate Viewed by the Camera in Coordinate Form
  </p>

<p align='center'>
  <img src="Images/Camera View.png">
  Figure #:
  </p>

### 3.3 Programming
<p align='center'>
  <img src="Images/Carmera Calibration.png">
  Figure #: Coppelia Code
  </p>

<p align='center'>
  <img src="Images/Connection Code.png">
  Figure #: Conection Code
  </p>
  
## 4. Controller Design and Simulations
### 4.1 Background
### 4.2 Simulink Diagram
<p align='center'>
  <img src="Images/SimulinkDiagram.JPG">
  Figure #: Simulink Diagram Used to Change the Angle of the Tray
  </p>

### 4.3 Codes
<p align='center'>
  <img src="Images/ballonplate1.JPG">
  </p>
  
<p align='center'>
  <img src="Images/ballonplate2.JPG">
  </p>


<p align='center'>
  Here is the link to the remApi.m PDF
  <img src="Images/remApi.m.pdf">
  </p>
  
<p align='center'>
  Here is the link to the remoteApiProto.m PDF
  <img src="Images/remoteApiProto.m.pdf">
  </p>

### 4.3

## 6. Checklist
Here is the link that shows the ball balancing on the plate
https://youtu.be/dRZi4ZY73e8
