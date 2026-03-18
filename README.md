# Speed Control for Planar Formation Tracking

[![MATLAB](https://img.shields.io/badge/MATLAB-Simulation-blue.svg)](https://www.mathworks.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the official simulation code for the paper: **"On Feedback Speed Control for a Planar Tracking"** by Xincheng Li, Tengyue Liu, and Udit Halder.

## Overview
While steering control in multi-agent formations is extensively studied, the role of active speed regulation is often overlooked. This repository provides the numerical simulations for a novel feedback speed control law paired with a constant bearing (CB) steering strategy. 

The control framework allows a follower agent (modeled as a nonholonomic unicycle) to maintain a rigid "abreast" formation (Bertrand mate) with a leader agent. The codebase includes simulations demonstrating:
1. **Ideal Tracking:** Asymptotic stability when the leader's steering effort is known.
2. **Leader-Independent Tracking:** Input-to-State Stability (ISS) and periodic orbit convergence when the leader's steering is unknown to the follower.
3. **N-Agent Chain Network:** Propagation of steering impulses through a multi-agent flock using cascaded pairwise tracking.

## Prerequisites
The numerical simulations are written in MATLAB and rely on standard built-in ODE solvers. No additional toolboxes are strictly required.
* **MATLAB** (Tested on R2023a or newer)

