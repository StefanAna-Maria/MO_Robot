# MO_Robot
Final project developed for the IR course.

<details>
  <summary>Introduction</summary>

## Ideea and Motivation:
The MO Robotics Project is inspired by the character MO from the animated series "Robotzi" by Creative Monkeys. MO is a quirky, humorous robot who works alongside his friend F.O.C.A in an experimental laboratory. In the series, MO is the more laid-back and scatterbrained of the duo, often causing trouble that F.O.C.A is left to fix. My project aims to bring MO to life by building a functional robot that captures his playful personality and clumsy charm.

This project is particularly meaningful to me as it allows me to combine my passion for robotics with nostalgic memories of a series I enjoyed watching during my childhood. By recreating MO, I hope to celebrate the creativity and humor of "Robotzi" while showcasing the potential of robotics to bring beloved characters to life.

## Functionality:
The MO Robot is designed as a faithful representation of the beloved character from the animated series Robotzi.

### The robot will feature:

- A single leg for mobility or stability.
- Two functional arms.
- LED matrix eyes capable of displaying animations.
- A mouth that can open and close.

### MO will have the ability to:

- Speak iconic lines from the series, capturing the character's humor and personality.
- Display eye animations using the LED matrix.
- Be controlled via a controller or remote, allowing for interactive operation.

### Additionally, MO will be programmed to interact with another robot, F.O.C.A.:

- Dialogue Mode: MO will engage in conversations with F.O.C.A.

</details>

<details>
  <summary>General Description</summary>
  
  - Description:
  - Block Scheme:
  TBD
</details>

<details>
  <summary>Hardware Design</summary>
  
  ## List of components:

  - 1X ESP32 WROOM
  - 1X LED Matrix
  - 4X Micro Servomotor
  - 1X Miniature Amplifier Module PAM8403
  - 1X Speaker
  - DC-DC Step Down Mini-360 Module
  - 2X LI-ION Well 18650 Battery (3.7V, 2200 mAh)
  - PCB Boards
  
  ## General Description:
  The ESP32-WROOM-32D serves as the main control unit for my project due to its compact design and built-in Bluetooth connectivity, enabling wireless control of the robot via a virtual remote and communication with other ESP32-based robots. The MAX7219 LED Matrix is used to display animations, specifically for creating expressive eye movements like blinking, giving the robot, MO, a dynamic personality. Four SG90 Micro Servo Motors control the robot's movements: two for the arms (moving forward and backward) and two for simulating mouth movements when the robot speaks. A PAM8403 Miniature Amplifier Module amplifies the sound output to a connected speaker, which plays the robot’s speech. Power is provided by two 18650 Li-ion Batteries (3.7V, 2200mAh), regulated via a DC-DC Step Down Module to ensure safe and stable voltage for all components. All components are carefully wired to specific GPIO pins on the ESP32 to ensure functionality, with a common ground setup and proper voltage regulation for stable operation.
  
  ---
  For a detailed description of every component used in this project please check [HERE](https://github.com/StefanAna-Maria/MO_Robot/blob/main/Hardware/README.md)
  
  ## Block Diagram:

  
  ## Electrical Diagram:

  
  ## Complete Circuit:
  TBD (I encountered issues regarding the delivery of some components)
  
  ## Images and Videos of the physical components:
  ### Arm prototype video:
  
  ### Test image and video for the LED Matrix:
  
  TBD
</details>

<details>
  <summary>Software Design</summary>
  TBD
</details>

<details>
  <summary>Results</summary>
  TBD
</details>

<details>
  <summary>Conclusions</summary>
  TBD
</details>

<details>
  <summary>Resources</summary>
  TBD
</details>
