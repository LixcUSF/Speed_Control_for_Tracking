# Numerical Simulations: Formation Tracking

This directory contains the MATLAB codebase used to numerically validate the cascaded speed and steering control laws for planar formation tracking.

## Overview
The simulation environment integrates the shape dynamics and unicycle kinematics of the multi-agent system using MATLAB's standard ODE solvers. It provides a purely mathematical testbed to verify:
* **Asymptotic Stability:** Ideal tracking under known leader inputs (Prop 3.1).
* **Input-to-State Stability (ISS):** Robust tracking under unknown leader maneuvers (Prop 3.2).
* **Periodic Orbits:** Convergence behavior under periodic leader steering (Prop 3.3).
* **N-Agent Flocking:** Wave-like propagation of steering impulses through a cascaded chain network.

## Prerequisites
* **MATLAB** (Tested on R2023a or newer). No specialized toolboxes are required.

## Directory Structure
* `bertrand_simulation_2agent.m`: The primary script for simulating the two-agent leader-follower formation.
* `bertrand_simulation_Nagent.m`: The script for simulating the N-agent chain network.
* `animate2p.m` and `animateN.m`: The script for visualizing the results of the simulations for the two-agent and N-agent case respectively.
* `Nparticles.slx`: The Simulink file for simulating the N-agent chain network.

## Usage
To run the two-agent simulation:
1. Open `bertrand_simulation_2agent.m` in MATLAB.
2. Toggle the control mode variable (e.g., `p.know = 1/0`) to test Prop 3.1 vs. Prop 3.2.
3. Run the script. It utilizes `ode45` with tolerances set to `1e-5` (relative) and `1e-6` (absolute).
4. The script will automatically output the 2D spatial trajectories and the polar coordinate phase portraits as well as a video animating the simulation results.
