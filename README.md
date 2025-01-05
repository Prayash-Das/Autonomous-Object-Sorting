# Autonomous Object Sorting Using a Mobile Robot

![Project Overview](./assets/project_overview.png)

This repository contains the implementation and report for the project **"Autonomous Object Sorting Using a Mobile Robot"**, completed as part of the course **ME 598-A: Introduction to Robotics** (Fall 2024). The project showcases the development of an autonomous mobile robot capable of detecting and sorting objects based on color in a constrained environment, while avoiding collisions and adhering to predefined operational guidelines.

---

## Project Overview

### Objective
Develop an autonomous system for sorting objects into their designated zones using a mobile robot equipped with:
- **Sensors:** A forward-facing color-detecting camera, odometry, and distance sensors.
- **Algorithm:** A finite state machine (FSM) for sequential task execution.

### Features
- Color-based object detection using HSV thresholds.
- Collision-free navigation with sensor-based obstacle avoidance.
- Efficient trajectory planning and task execution.
- Visualization of robot trajectories in MATLAB.

---

## File Structure

### Key Files
- **`ME598FinalProject.slx`**: Simulink file containing the project implementation.
- **`ME598A_GR2_Final_Project_report.pdf`**: Comprehensive report documenting the project details, including theory, methodology, results, and insights.
- **`trajectory_plot.m`**: MATLAB script to visualize the robot's trajectory.

---

## Getting Started

### Prerequisites
1. MATLAB R2023b or later with Simulink installed.
2. Required MATLAB toolboxes:
   - Robotics System Toolbox
   - Control System Toolbox
   - Image Processing Toolbox
3. A compatible environment for running the simulation (Windows/Mac/Linux).

### Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/<your-username>/autonomous-object-sorting.git
    cd autonomous-object-sorting
    ```
2. Open the Simulink file `ME598FinalProject.slx` in MATLAB.

---

## How to Use

### Running the Simulation
1. Launch MATLAB and navigate to the project directory.
2. Open `ME598FinalProject.slx`.
3. Run the simulation to observe:
   - Object detection and sorting process.
   - Collision avoidance.
   - Robot's trajectory and task execution.

### Visualizing the Trajectory
1. Run the MATLAB script `trajectory_plot.m` to generate an overhead XY plot of the robot's trajectory:
    ```matlab
    run('trajectory_plot.m')
    ```
   ![Trajectory Plot](./assets/trajectory_plot.png)

---

## Results
The robot successfully completed all six trials under varying initial conditions with:
- **Accuracy:** 100% success rate in object detection and sorting.
- **Performance:** Average completion time of 62.1 seconds.
- **Best Trial:** Red and Blue objects, completed in 60.2 seconds.

---

## Key Challenges & Solutions
1. **Color Detection:**
   - Challenge: Inconsistent detection under varying lighting conditions.
   - Solution: Implemented dynamic HSV thresholding and Gaussian filtering.

2. **Path Planning:**
   - Challenge: Deviations in robot trajectory.
   - Solution: Fine-tuned PD controller gains and added position correction logic.

3. **Object Alignment:**
   - Challenge: Misalignment during pickup.
   - Solution: Improved centroid detection and introduced tolerance margins.

---

## Future Work
1. Incorporate advanced path optimization algorithms (e.g., A*).
2. Integrate real-time obstacle detection for dynamic environments.
3. Leverage machine learning for enhanced object recognition and adaptive navigation.

---

## Contributors
- **Mohammad Althaf Syed**
- **Bhagyath Badduri**
- **Matthew Casey**
- **Prayash Das**

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- Stevens Institute of Technology
- Professor for ME 598-A: Introduction to Robotics
- Course materials and MATLAB resources

For more details, please refer to the [project report](./ME598A_GR2_Final_Project_report.pdf).
