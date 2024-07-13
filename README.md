# Calculating-inverse-and-forward-kinematics
Calculate inverse and forward kinematics for a robot with 3 degrees of freedom

## introduction:
- In robotics, Inverse Kinematics and Forward Kinematics are fundamental processes.
- Forward Kinematics: This process calculates the location and direction of the robot's end-effector based on the angles of the different joints.
- Inverse Kinematics: While the Inverse Kinematics process does the opposite, it calculates the joint angles necessary to achieve a specific location and direction for the manipulator.

  ## Suppose we have a robotic arm that has 3 degrees of freedom (3-DOF). How will we calculate both forward and backward kinematics?

  ### Forward Kinematics:
  #### Robotic Arm Definition
 We will name each joint angle as θ₁, θ₂, and θ₃. Additionally:
  - The length between joints 1 and 2 is L1.
  - The length between joints 2 and 3 is L2.
  - The length between joint 3 and the end effector is L3.
  - The spatial angle (φ) between the X, Y, and Z axes

  #### Equations:
 To compute the final position (x, y, z) of the end effector, we use the following equations considering the spatial angle φ:
 ```
x=L1cos(θ1)+L2cos(θ1 +θ2 )+L3cos(θ1 +θ2 +θ3 ))cos(ϕ)

y=L1cos(θ1 )+L2cos(θ1 +θ2 )+L3cos(θ1+θ2+θ3))sin(ϕ)

z=L1sin(θ1 )+L2sin(θ1 +θ2 )+L3sin(θ1+θ2+θ3))
```
### Example:

#### Assume:
- L1=1meter
- L2=1meter
- L3=1meter
- The angles are θ1=30∘,θ2=45∘,θ3=60∘
- The spatial angle ϕ=30∘
  
#### First, convert the angles from degrees to radians:
- θ1=30∘=π/6 radians
- θ2=45∘=π/4 radians
- θ3=60∘=π/3 radians
  
#### Apply the equations:

- x=1cos(π/6)+1cos(π/6 +π/4)+1cos(π/6 +π/4 +π/3))cos(π/6)

- y=1cos(π/6)+1cos(π/6 +π/4)+1cos(π/6 +π/4 +π/3))sin(π/6)

- z=1sin(π/6)+1sin(π/6 +π/4)+1sin(π/6 +π/4 +π/3))

### Inverse Kinematics in Three Dimensions:
#### Objective:
Calculate the angles 𝜃1,𝜃2,and 𝜃3 that result in the final position (x, y, z).
#### Equations:

1- Calculate the spatial angle 𝜙:

![Screenshot 2024-07-13 195508](https://github.com/user-attachments/assets/ef22e58d-5c60-484c-9e5b-76f39eb84ef5)


2- Calculate the horizontal distance 𝑟:

![556](https://github.com/user-attachments/assets/47039242-a3e3-4ef3-9404-4110e9c2d324)

3- Calculate the angles 𝜃1 ,𝜃2 , and 𝜃3 :

![---](https://github.com/user-attachments/assets/f81a6a7c-81ee-4021-8f94-2f51d595705f)

Then use trigonometric equations to calculate 𝜃2 and 𝜃3 :

![000k](https://github.com/user-attachments/assets/b7fcf912-0db1-4346-b966-a3c0f2c27a63)


​



 
