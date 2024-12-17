# MO_Robot
### Final project developed for the IR course.

<details>
  <summary><h2>Introduction</h2></summary>

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
  <summary><h2>General Description</h2></summary>
  
  - Description:
  - Block Scheme:
  ![Screenshot 2024-12-17 211839](https://github.com/user-attachments/assets/44acc22f-ad5b-4283-95f1-bf062ffcd20f)

</details>

<details>
  <summary><h2>Hardware Design</h2></summary>
  
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
  ![Screenshot 2024-12-17 211839](https://github.com/user-attachments/assets/c9596389-4a8e-40e2-843a-411d9e57200c)

  ## Electrical Diagram:
 ![Screenshot 2024-12-17 205839](https://github.com/user-attachments/assets/b9d76cd3-2725-41ec-b41a-44b96dac35ec)

  ## Complete Circuit:
  TBD (I encountered issues regarding the delivery of some components)
  
  ## Images and Videos of the physical components:
  ### Arm prototype video:
  
  ### Test image and video for the LED Matrix:
  
  TBD
</details>

<details>
  <summary><h2>Software Design</h2></summary>
  TBD
</details>

<details>
  <summary><h2>Results</h2></summary>
  TBD
</details>

<details>
  <summary><h2>Conclusions</h2></summary>
  TBD
</details>

<details>
  <summary><h2>Resources</h2></summary>

  - [ESP32-WROOM-32D DATASHEET](https://www.espressif.com/sites/default/files/documentation/esp32-wroom-32d_esp32-wroom-32u_datasheet_en.pdf)
  - [LED Matrix Module MAX7219 DATASHEET](https://www.analog.com/media/en/technical-documentation/data-sheets/MAX7219-MAX7221.pdf)
  - [Micro Servomotor SG90 90° DATASHEET](https://www.friendlywire.com/projects/ne555-servo-safe/SG90-datasheet.pdf)
  - [Speaker DATASHEET](https://www.farnell.com/datasheets/2827522.pdf)
  - [Miniature Amplifier Module PAM8403 DATASHEET](https://www.mouser.com/datasheet/2/115/PAM8403-247318.pdf)
  - [DC-DC Step Down Mini-360 Module DATASHEET](https://www.matts-electronics.com/wp-content/uploads/2018/06/MINI-360.pdf)

  ![Screenshot 2024-12-12 194316](https://github.com/user-attachments/assets/111ab6f2-bc48-4e6e-a156-49e5d9ca6c17)

  
</details>
