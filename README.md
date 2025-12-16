# Exploring Motion Matching and Animation Retargeting in UE5

# 📑 Index

- [Project Goal](#-project-goal)
- [Requirements](#️-requirements-and-plugins)
- [Project Structure](#️-project-structure)
- [Implementation](#-implementation)
  - [Motion Matching and Retargeting](#motion-matching-and-retargeting)
  - [Metahuman](#metahuman)
- [Results](#-results)  
- [Authors](#-authors)


# 🎯 Project Goal
The purpose of this project is to become familiar with **Motion Matching**, **Retargeting** and  **MetaHuman** in **Unreal Engine 5**, exploring their workflows and practical applications in character animation.

- **Motion Matching**: is an animation technique that dynamically selects the most appropriate animation pose from a large database of motion data in real time. Instead of relying on predefined animation states and transitions, the system continuously compares the character’s current pose and movement intent with the available animation data, resulting in smoother, more natural, and more responsive character movement.

- **Retargeting**: is the process of transferring animations from one skeletal mesh to another with a different skeleton structure or proportions. Unreal Engine 5’s retargeting system allows animations created for a source character to be accurately adapted to a target character, preserving motion quality while reducing the need to recreate animations for each new character.

- **MetaHuman**: as part of this project, MetaHuman characters are explored to test and validate motion matching and retargeting workflows on digital humans.

# ⚙️ Requirements and Plugins

We used **Unreal Engine 5.6**.  
Enable the following **Plugins** in UE:
- Pose Search
- Motion Trajectory
- Animation Warping
- Motion Warping
- Animation Locomotion Library
- Deformer Graph
- Chooser
- Metahuman Creator
- Metahuman Core Tech

# 🗂️ Project Structure

Here we put only the most important files of our project:

# 📋 Implementation

## Motion Matching and Retargeting

1. For the motion matching we import the animation of the [Game Animation Sample Project](https://dev.epicgames.com/documentation/en-us/unreal-engine/game-animation-sample-project-in-unreal-engine)
2. Perform animation retargeting using our custom character
3. Set the same skeleton on the Third Person Character Blueprint
4. Create a MotionMatching folder; create a Pose Search Schema using the same skeleton selected before; Create a databases folder;create a Pose Search Database for each desired action (Idle, Walk, Run, Jump, Crouch) (TODO: insert screenshot)
5. Add the retargeted animations (point 2) to their corresponding databases.
6. Add the Character Trajectory component to the Third Person Character Blueprint
7. Create a new Animation Blueprint using the same skeleton
8. Build the following graph in the EventGraph (TODO: insert screenshot)
9. Build the following graph in the AnimGraph (TODO: insert screenshot)
10. Create a Chooser Table: chooser type: Animation Chooser, Anim Class: ABP_MQ; output: PoseSearchDatabase.  
    Fill the table with 5 row for every action (idle, walk, run, jump, crouch) and 3 column for speed, isFalling and is Crouching.
11. Configure the table values to match the setup shown in the following image: (TODO: insert screenshot)

Note: To visualize the trajectory, simply add the Character Trajectory to the character component. Then, from the Unreal Engine console, run the following command: ```a.CharacterTrajectory.Debug 1```

## Metahuman 

### 1.
### 2.
### 3.
### 4.



# 🎮 Results

# 👥 Authors

Nicola Cappellaro - nicola.cappellaro@studenti.unitn.it  
Riccardo Zannoni  - riccardo.zannoni@studenti.unitn.it



<p align="center">
  <img src="gif_results/04_yolo.gif" width="45%" />
  <img src="gif_results/03_final_mocap.gif" width="45%" />
</p>


<p align="center">
  <img src="gif_results/UE_render.gif" width="90%" />
</p>
