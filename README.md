# Calculating-inverse-and-forward-kinematics
Calculate inverse and forward kinematics for a robot with 3 degrees of freedom

## introduction:
- In robotics, Inverse Kinematics and Forward Kinematics are fundamental processes.
- Forward Kinematics: This process calculates the location and direction of the robot's end-effector based on the angles of the different joints.
- Inverse Kinematics: While the Inverse Kinematics process does the opposite, it calculates the joint angles necessary to achieve a specific location and direction for the manipulator.

  ## Suppose we have a robotic arm that has 3 degrees of freedom (3-DOF). How will we calculate both forward and backward kinematics?

  ### Forward Kinematics:
  #### Robotic Arm Definition
  We will name each joint angle as θ₁, θ₂, and θ₃. The assumptions are:
  - The length between joints 1 and 2 is L1.
  - The length between joints 2 and 3 is L2.
  - The length between joint 3 and the end effector is L3.

  #### Equations:
  To compute the final position (x, y, z) of the end effector, we use the following equations:
 ```
x=L1cos(θ1)+L2cos(θ1 +θ2 )+L3cos(θ1 +θ2 +θ3 )

y=L1sin(θ1 )+L2sin(θ1 +θ2 )+L3sin(θ1+θ2+θ3)
```
