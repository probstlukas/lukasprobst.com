---
layout: page
title: Integration of Real and Simulated ALOHA Robots
description: Imitation learning with teleoperation, simulation, and Movement Primitive Diffusion
img: assets/img/projects/alr_research_project/colliders_drawer_knob_view.png
importance: 2
category: research
related_publications: false
---

## Overview

As part of the Research Project Autonomous Learning Robots at KIT, I worked on integrating real and simulated ALOHA robots for imitation learning. The goal was to create a workflow in which human demonstrations could be performed through the [ALOHA](https://github.com/tonyzhaozh/aloha) teleoperation interface inside [NVIDIA Isaac Lab](https://github.com/isaac-sim/IsaacLab), recorded efficiently, and then used to train robot policies for manipulation tasks.

The project focused on connecting teleoperation, simulation, dataset recording, and policy execution into one coherent pipeline. We explored tasks such as table sweeping, block picking, and block transfer, and used Movement Primitive Diffusion (MPD) to learn fine-grained robot behaviour from demonstrations.

## What I worked on

- Integrated the ALOHA teleoperation interface with the simulation environment
- Helped build a recording pipeline for collecting demonstrations as structured training data
- Worked on the connection between the simulation setup and the MPD training workflow
- Evaluated how imitation learning can be used to transfer demonstrated behaviour to robotic manipulation tasks
- Contributed to a modular setup that kept repositories separated while still enabling real-time communication

## Technical highlights

The system used the ALOHA master setup for teleoperation while the robot acted inside simulation. To avoid tightly coupling repositories, the integration relied on Python multiprocessing and local communication of joint-angle data. Demonstrations were recorded during simulation and stored as NumPy `.npz` files, which could then be used directly for training. After training, the learned model was deployed back into the same simulation environment for validation.

This setup made it possible to iterate quickly and safely in simulation before considering transfer to real-world robotic applications.

## Why I found it interesting

I liked this project because it combined several things I enjoy working on:

- robot learning
- simulation-based experimentation
- practical systems integration
- imitation learning for fine-grained manipulation

It was a great introduction to research at the intersection of robotics and machine learning, especially the challenge of bridging real hardware interfaces with scalable simulation workflows.

## Report

You can read the full project report here:

- [Project Report (PDF)](/assets/pdf/2024_Praktikum_ALR_Fricke_Probst.pdf)

## Links

- [Teleoperation interface with simulation connection](https://github.com/probstlukas/aloha-group4)
- [Extended Movement Primitive Diffusion repository](https://github.com/probstlukas/movement-primitive-diffusion)
- ALOHA simulation repository (currently private, part of ALRhub intellectual property)

## Project context

This project was completed at Karlsruhe Institute of Technology (KIT) as part of the Research Project Autonomous Learning Robots module.
