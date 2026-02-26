# Robot-Navigation-Using-Subsumption-Architecture-and-Unicycle-Kinematics
This project implements an autonomous robot navigation system in MATLAB using Subsumption Architecture for layered, priority-based behaviors. The robot navigates a 2D environment while avoiding obstacles and seeking a goal, following the unicycle kinematic model for realistic motion.
Subsumption Architecture
The subsumption architecture, developed by Rodney Brooks in the mid-1980s, is a behavior-based, decentralized approach to robot control. Instead of relying on a centralized decision-making system, it layers simple reactive behaviors to produce complex actions.
Key Features:
Behavior Layers:
Each layer handles a specific task (e.g., obstacle avoidance, wandering, goal seeking).
Higher-priority layers can override lower-priority layers to ensure safety and goal-directed behavior.
Reactive Control:
Behaviors respond directly to sensor inputs without complex planning or global world models.
Prioritization:
Critical behaviors (e.g., avoiding collisions) take precedence over less critical ones (e.g., seeking a goal).
Parallel Processing:
All behavior layers run concurrently, allowing the robot to adapt quickly to dynamic environments.
Objective
Design, implement, and simulate a robot navigation system in a 2D environment where the robot:
Navigates towards a goal
Avoids obstacles using priority-based behaviors
Follows the unicycle kinematic model
Learning Outcomes
By completing this project, you will:
Understand and implement the subsumption architecture
Apply the unicycle kinematic model for robot motion
Develop a simulation environment for navigation testing
Gain hands-on experience with MATLAB for robotics
Task Description
Environment Setup
Create a 2D environment
Randomly place ≥20 circular obstacles
Define a goal position
Robot Representation
State: (x, y, θ) where x, y = position, θ = orientation (radians)
Motion follows the unicycle kinematic model:
x_dot = v * cos(θ)
y_dot = v * sin(θ)
θ_dot = ω
where v = linear velocity, ω = angular velocity
Behavior Design
Implement three behaviors:
Obstacle Avoidance (highest priority):
Calculate repulsion forces to avoid obstacles within a certain radius
Random Wander (medium priority):
Explore the environment randomly
Goal Seeking (lowest priority):
Navigate towards the goal position
Use subsumption architecture to prioritize these behaviors
Control Inputs
Calculate v (linear velocity) and ω (angular velocity) based on prioritized behavior
Limit v and ω to safe values
Simulation
Simulate motion for up to 300 steps or until the robot reaches the goal (within 2 units)
Visualization
Plot environment:
Obstacles: red circles
Goal: green circle
Robot: blue dot
Update robot position in real-time
Report
Comment your code explaining:
Design of the behaviors
Implementation of the subsumption architecture
Observations from simulation (e.g., challenges, time to reach goal)
Requirements
Implement the program in MATLAB
Follow the unicycle kinematic model
Use modular programming (separate functions for behaviors and subsumption logic)
Deliverables
main.m – main simulation script
Separate MATLAB function files for:
Obstacle Avoidance
Random Wander
Goal Seeking
Subsumption logic
