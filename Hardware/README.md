## Description
Here you can find a description of each component's purpose and its pin connections used in building my robot, MO.

<details>
  <summary>ESP32-WROOM-32D</summary>

  The ESP32-WROOM-32D acts as the central control unit of the robot, chosen for its compact design, powerful processing capabilities, and integrated Bluetooth connectivity. Bluetooth is essential for remotely controlling the robot’s movements via a virtual remote, as well as for facilitating communication with another robot using the same ESP32 platform. The board powers peripheral components, including servos, an LED matrix, and an amplifier, with all components sharing a common ground. Specific GPIO pins are used to connect modules and peripherals for proper operation.
</details>

<details>
  <summary>MAX7219 LED Matrix</summary>

  The MAX7219 LED Matrix is used to create dynamic animations for the robot's eyes, adding personality by simulating blinking and movement. This module requires a data line (DIN) for receiving commands, connected to GPIO 23 of the ESP32. The chip select (CS) pin is connected to GPIO 5, while the clock (CLK) signal is managed by GPIO 18. Power is supplied through the 5V pin, ensuring compatibility with the ESP32’s voltage output. The second matrix is cascaded by connecting its DIN input to the first matrix's DOUT, sharing the same VCC, GND, and signal pins.
</details>

<details>
  <summary>SG90 Micro Servo Motors</summary>

  The project utilizes four SG90 micro servos to control the robot’s physical movements. Two servos are assigned to move the robot’s arms forward and backward, while the other two operate the mouth to simulate speech. Each servo’s Signal pin is connected to a dedicated ESP32 GPIO pin: GPIO 13, GPIO 12, GPIO 28, and GPIO 27, respectively. The servos are powered via a regulated 5V output from the DC-DC Step Down Module, ensuring stable voltage and avoiding current fluctuations. The ground (GND) of all servos is tied to the common GND of the circuit.
</details>

<details>
  <summary>PAM8403 Miniature Amplifier Module</summary>

  The PAM8403 amplifier module enhances the audio output for the robot’s speech system. Its L-IN/R-IN inputs are connected to GPIO 25 on the ESP32, which transmits the audio signal. Power for the amplifier is provided through the Step Down Module’s OUT+, delivering a steady 5V. The amplifier outputs sound through a connected speaker, with terminals wired to the amplifier’s speaker outputs. A shared GND ensures smooth operation and minimizes noise in the audio output.
</details>

<details>
  <summary>Speaker</summary>

  The speaker emits sound corresponding to the robot's speech, made possible through the PAM8403 amplifier module. The speaker terminals are directly connected to the amplifier’s output pins. The amplifier ensures sufficient audio gain, while the ESP32 provides the signal through GPIO 25. This combination allows the speaker to produce clear and amplified sound.
</details>

<details>
  <summary>DC-DC Step Down Mini-360 Module</summary>

  The DC-DC Step Down Mini-360 module regulates voltage from the 18650 Li-ion batteries. The battery’s positive terminal is connected to the IN+ pin, while the negative terminal connects to IN-. The module outputs a stable 5V through the OUT+ pin, supplying power to the servos and PAM8403 amplifier. The OUT- is connected to the common ground of the system, ensuring consistent and safe voltage distribution for all components.
</details>

<details>
  <summary>18650 Li-ion Batteries</summary>

  I used two 18650 Li-ion batteries (3.7V, 2200mAh) to act as the power source for the entire system. Their combined voltage is regulated by the DC-DC Step Down Module, which outputs 5V for the LED matrix, servos and amplifier. The batteries positive and negative terminals connect to the IN+ and IN- pins of the Step Down module, providing continuous and portable power for the robot.
</details>

## Table of PIN connections
This table provides a clear mapping of pins and connections for my ESP32-WROOM-32D project.

| **Component**               | **Pin**         | **ESP32 Pin / Other**       |
|-----------------------------|-----------------|-----------------------------|
| **LED Matrix Module 1**     | VCC             | 5V                          |
|                             | GND             | GND                         |
|                             | DIN             | GPIO 23                     |
|                             | CS              | GPIO 5                      |
|                             | CLK             | GPIO 18                     |
| **LED Matrix Module 2**     | DIN (from DOUT) | Matrix 1 **DOUT**           |
|                             | VCC             | 3.3V                        |
|                             | GND             | GND                         |
| **Micro Servo 1 (SG90)**    | VCC             | Step Down **OUT+**          |
|                             | GND             | GND                         |
|                             | Signal          | GPIO 13                     |
| **Micro Servo 2**           | Signal          | GPIO 12                     |
| **Micro Servo 3**           | Signal          | GPIO 28                     |
| **Micro Servo 4**           | Signal          | GPIO 27                     |
| **PAM8403 Amplifier**       | VCC             | Step Down **OUT+**          |
|                             | GND             | GND                         |
|                             | L-IN / R-IN     | GPIO 25                     |
|                             | Speaker Output  | Speaker terminals           |
| **DC-DC Step Down**         | IN+             | Battery Positive            |
|                             | IN-             | Battery GND                 |
|                             | OUT+            | Servos / PAM8403 VCC        |
|                             | OUT-            | Common GND                  |
| **18650 Batteries**         | Positive        | Step Down **IN+**           |
|                             | Negative        | Step Down **IN-**           |

---

### Notes
1. **Ground Connections**: All components share a **common ground** for proper operation.
2. **Power Supply**: Used the Step-Down Module to provide a steady 5V for servos and PAM8403, and 3.3V for the ESP32 and LED matrices.

## Bill of Components

| Quantity | Material                                   | Link to shop  										                                                                         | Datasheet     |
|----------|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
|    1     | ESP32-WROOM-32D                            | [SHOP LINK](https://www.sigmanortec.ro/placa-dezvoltare-esp32-cu-wifi-si-bluetooth)   										 | [DATASHEET](file:///C:/Users/anama/Downloads/esp32-wroom-32d_esp32-wroom-32u_datasheet_en.pdf) |
|    1     | LED Matrix Module MAX7219                  | [SHOP LINK](https://www.optimusdigital.ro/ro/optoelectronice-matrice-de-led-uri/118-modul-cu-matrice-de-led-uri-max7219.html?search_query=matrice+led&results=51)      | [DATASHEET](file:///C:/Users/anama/AppData/Local/Microsoft/Windows/INetCache/IE/D0JNYWEH/MAX7219-Datasheet[1].pdf) |
|    4     | Micro Servomotor SG90 90°                  | [SHOP LINK](https://www.optimusdigital.ro/ro/motoare-servomotoare/26-micro-servomotor-sg90.html?search_query=servomotor&results=116)               			 | [DATASHEET](file:///C:/Users/anama/AppData/Local/Microsoft/Windows/INetCache/IE/D0JNYWEH/Foaie%20de%20Catalog%20Servo%20Motor%20SG90[1].pdf) |
|    1     | Speaker (1 W)                              | [SHOP LINK](https://www.optimusdigital.ro/ro/audio-difuzoare/2147-difuzor-de-1-w.html?search_query=difuzor&results=95&HTTP_REFERER=https%3A%2F%2Fwww.optimusdigital.ro%2Fro%2Fcautare%3Fcontroller%3Dsearch%26orderby%3Dposition%26orderway%3Ddesc%26search_query%3Ddifuzor%26submit_search%3D)               															 |       X       |
|    1     | Miniature Amplifier Module PAM8403(2.2-5 V)| [SHOP LINK](https://www.sigmanortec.ro/modul-amplificator-miniatura-pam8403-22-5v?gad_source=1)               							 | [DATASHEET](https://www.mouser.com/datasheet/2/115/PAM8403-247318.pdf) |
|    1     | DC-DC Step Down Mini-360 Module            | [SHOP LINK](https://www.optimusdigital.ro/ro/surse-coboratoare-reglabile/152-modul-dc-dc-step-down-mini-360.html?search_query=modul+dc-dc+step+down+mini+360&results=1)|       X       |
|    2     | LI-ION Well 18650 battery (3.7V, 2200 mAh) | [SHOP LINK](https://www.dedeman.ro/ro/acumulator-li-ion-well-18650-3-7v-2200-mah/p/1050265)  										 |       X       |
|    1     | PCB board                                  | [SHOP LINK](https://www.sigmanortec.ro/Placa-PCB-prototipare-fata-dubla-7x9cm-p125747328)               								 |       X       |

## Block Scheme
TBD
## Circuit Diagram
TBD
