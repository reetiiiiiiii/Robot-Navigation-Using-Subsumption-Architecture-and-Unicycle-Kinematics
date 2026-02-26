# Robot-Navigation-Using-Subsumption-Architecture-and-Unicycle-Kinematics

This project implements an **autonomous robot navigation system** in MATLAB using **Subsumption Architecture** for layered, priority-based behaviors. The robot navigates a 2D environment while avoiding obstacles and seeking a goal, following the **unicycle kinematic model** for realistic motion.

---

## Subsumption Architecture

The **subsumption architecture**, developed by Rodney Brooks in the mid-1980s, is a **behavior-based, decentralized approach** to robot control. Instead of relying on a centralized decision-making system, it layers simple reactive behaviors to produce complex actions.

**Key Features:**

- **Behavior Layers:**  
  Each layer handles a specific task (e.g., obstacle avoidance, wandering, goal seeking).  
  Higher-priority layers can override lower-priority layers to ensure safety and goal-directed behavior.

- **Reactive Control:**  
  Behaviors respond directly to sensor inputs without complex planning or global world models.

- **Prioritization:**  
  Critical behaviors (e.g., avoiding collisions) take precedence over less critical ones (e.g., seeking a goal).

- **Parallel Processing:**  
  All behavior layers run concurrently, allowing the robot to adapt quickly to dynamic environments.

---

## Objective

Design, implement, and simulate a robot navigation system in a 2D environment where the robot:

- Navigates towards a goal  
- Avoids obstacles using priority-based behaviors  
- Follows the unicycle kinematic model  

---

## Learning Outcomes

By completing this project, you will:

- Understand and implement the **subsumption architecture**  
- Apply the **unicycle kinematic model** for robot motion  
- Develop a **simulation environment** for navigation testing  
- Gain hands-on experience with **MATLAB for robotics**  

---

## Task Description

### Environment Setup
- Create a **2D environment**  
- Randomly place **≥20 circular obstacles**  
- Define a **goal position**  

### Robot Representation
- State: `(x, y, θ)` where `x, y` = position, `θ` = orientation (radians)  
- Motion follows the **unicycle kinematic model**:  

```matlab
x_dot = v * cos(theta);
y_dot = v * sin(theta);
theta_dot = omega;
