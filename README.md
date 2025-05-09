# Control Strategies for Trajectory Tracking - Comparative Study

This project presents a comparative study of multiple
control strategies for trajectory tracking in autonomous
mobile robots. Leveraging 2D LIDAR-based SLAM for
trajectory generation, we evaluate the performance of
six controllers—PID, PD, MPC, Fast MPC, LQR, and
LQG—under varying speed conditions. The analysis
focuses on tracking accuracy using cross track error as
the key performance metric. Our findings offer insights
into the trade-offs between classical and optimal control
methods, highlighting their respective strengths, limita-
tions, and suitability for real-world navigation tasks.


## 🚀 Features

- ✅ 2D Lidar SLAM generated trajectory from a dataset
- ✅ Robot state update using kinematic equations (unicycle model)
- ✅ PID and PD controller with anti-windup and heading-based speed scaling
- ✅ MPC controller with discrete control search over prediction horizon
- ✅ Fast MPC version optimized for speed and responsiveness
- ✅ Fully integrated Simulink simulation environment
- ✅ Visualization and export of XY trajectory plots

## File Description

[`SLAM_based_control_system.mlx`](./SLAM_based_control_system.mlx)
- MATLAB notebook script with trajectory generation code. This notebook also includes the pipeline for data preprocessing, analysis and extraction of the trajectory once it is generated from Lidar Data. Here we are using the Lidar toolbox for trajectory generation. This script also consists of controller functions that we used in designing the simulink models. These functions were first built in python which you can find here [`main.py`](./main.py).


[`main.py`](./main.py)
- Main.py file contains the python script that includes all the controllers we designed and modelled for the trajectory tracking task for a differential drive robot. It also contains the simulation and analysis part inside the same simulation for the correct visualization and to draw some comparative analysis. It uses the trajectory that is generated by the MATLAB file mentioned above.

`Results #mps`
- The results generated by the main.py file above can be viewed along with the simulation for velocities from 1 m/s to 5 m/s for the d-drive robot to keep itself sane with the trajectory in these folders.

[`Simulink`](./Simulink)
- This folder contains all the simulink models for the controllers we used for this analysis. The .pdf file contain all the information about a single controller. In the output folder there are plots for the simulation of these controllers to make the robot follow the same trajectory. We can also find the overshoot and settling behavior in the project report.

 [`Controller Strategies for Trajectory Tracking – Final Report (PDF)`](./Controller%20Strategies%20for%20Trajectory%20Tracking%20Final%20Report.pdf)
 - You can read the full project report here.
  
