# Robotics assignment 3
The project simulates a robotic platform in various environments, implementing mapping, static navigation, and dynamic obstacle avoidance. These tasks are executed in a simulated environment using the TurtleBot3 model.
## STEP 1 - MAPPING AND EXPLORING THE MAP
the robot autonomously explores a random, closed environment to create a comprehensive map. The mapping is achieved using an occupancy grid combined with frontier exploration. The robot employs the K-means algorithm for determining frontiers and then uses the A* algorithm to navigate to these frontiers. This efficient mapping strategy completes the task in approximately 4 minutes on the test environment.
 
## STEP 2 - STATIC NAVIGATION
Building on the map created in Task 1, the robot is now required to navigate to arbitrary points within this mapped environment. This task also utilizes the A* algorithm for path planning
## STEP 3 - Autonomous Navigation (dynamic obstacles)
The final step introduces moving obstacles in the environment. The robot, equipped with LIDAR, dynamically adjusts its path to avoid these obstacles. The control algorithm creates a topographical representation of the environment, with obstacles forming 'peaks' and safe areas forming 'valleys,' guiding the robot through safe paths and allowing it to return to its original path whenever feasible


Getting Started

Follow these steps to set up and run the project tasks:

## 1. Clone and Build:
   - Clone this repository to your workspace's `src` folder.
   - Navigate to your workspace directory and run `catkin_make` or `catkin build`.

## 2. Set Environment Variable:
   - Set the robot model environment variable:
     
     export TURTLEBOT3_MODEL=waffle
     

## 3. Source the Package:
   - In your workspace directory, source the setup file:
  
     source devel/setup.bash
     

 Running the Tasks

## 1. step 1 - Autonomous Mapping:

   roslaunch final_project mapping.launch
   
   - (After mapping the environment, save the map in a new terminal):
  
     rosrun map_server map_saver -f map
     

## 2. step 2 - Static Navigation:

   roslaunch final_project static.launch
   

## 3. step 3 - Dynamic Obstacle Navigation:

   roslaunch final_project dynamic.launch

