# 3806ICT Final Assignment 3 by:

-  Omar Thompson| s5327969 
-  Hayley Naidoo | s5225359
-  Thomas Smith | s5333902
-  William Smallacomb | s5400330


This project requires an Ubuntu environment with ROS, Gazebo, and PAT installed. It is meant to improve on an existing implementation of the same system, structure and code by prioritising the implementation of a Heirarchial AI agent decision making structure. 

Gazebo simulates the environment and provides a 3D representation in real-time. ROS drives the  main control loop, which extracts a list of moves from PAT. PAT then using a Heirarchial Decision making structure interprets the input, makes a plan, executes and then validates that it works. 

To successfully run this project on your own machine:

1. Clone this repository into the catkin workspace folder (under catkin_ws/src).
2. Compile the binaries in catkin_ws/src using catkin_make.
3. Launch the pre-set world which includes a birds-eye camera angle:
   `roslaunch assignment_3 launch_world.launch`
4. Run the update_grid node: `rosrun assignment_3 update_grid` in a new terminal window. 
5. Run the search_rescue node: `rosrun assignment_3 search_rescue`

With the implementation of the new decsion making structure the program is more reusable, provides modularity, introduces deliberative reasoning that is goal focussed.


**Please note that the project depends on the direct path to the PAT installation. Currently, it is set to `/Desktop/MONO-PAT-v3.6.0/PAT3.Console.exe`. If this path is incorrect, either relocate PAT to the expected path, or change `PAT_EXE_DIR` in the program to the correct path. This `#define` is located in `search_rescue.cpp` on line 29**
