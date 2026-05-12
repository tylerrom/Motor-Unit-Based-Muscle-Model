
## Overview
[2]This project simulates a motor unit pool based on **Henneman’s Size Principle**  [5]and the **Fuglevand Model**. It compares a static algebraic model against a dynamic system governed by first-order activation kinetics. The simulation highlights the biological "speed limit" of muscle tissue, quantifying the phase lag between neural command and force production using the **Euler Method**.

## Features
* [5]**Fuglevand Model Implementation:** Exponential distribution of recruitment thresholds and maximum forces.
* [5]**Dynamic Activation:** Modeling muscle activation dynamics as a low-pass filter using a first-order ODE[cite: 5].
* **Numerical Methods:** * **Euler Method:** Used to solve the differential equation for activation over time.
    * **Trapezoidal Rule:** Applied to calculate the Total Mechanical Work ($W$) by integrating the force-time curve.
* **Visualization:** Dual-axis plotting to compare Neural Drive (input) against Force Output (output), highlighting the 150ms phase lag.

## How to Run the Code
To run this simulation on your local machine, follow these steps:

### 1. Prerequisites
Ensure you have **Python 3.x** installed along with the following libraries:
* `numpy`: For numerical calculations.
* `matplotlib`: For generating the plots.

You can install these via terminal/command prompt using:
```bash
pip install numpy matplotlib
2. Execution Environment:
This code is designed to be run in a Jupyter Notebook (.ipynb) or a standard Python IDE (like VS Code or Spyder)
* Jupyter: Paste the code into a cell and press Shift + Enter
* Python Script: Ensure you have a window manager installed to view the matplotlib pop-up.3. 
Running the Simulation
* Initialize Parameters: The first section sets up the 15 motor units and the time constant ($\tau = 0.15$)
* Generate Drive: The script creates a sine-wave neural drive to simulate a rhythmic contraction
* Compute Forces: The code calculates the static force and the dynamic (ODE-solved) force.View Results: A plot will generate showing the Neural Drive, Static Force, and Dynamic Force.Project Structure
* Recruitment Logic: Simulates 15 motor units with varying thresholds.  
* Neural Drive: A sine-wave input representing the "brain signal."
