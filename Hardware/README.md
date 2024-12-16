## Description

This table provides a clear mapping of pins and connections for my ESP32-WROOM-32D project.

| **Component**               | **Pin**          | **ESP32 Pin / Other**       |
|-----------------------------|------------------|-----------------------------|
| **LED Matrix Module 1**     | VCC             | 3.3V                        |
|                             | GND             | GND                         |
|                             | DIN             | GPIO 23                     |
|                             | CS              | GPIO 5                      |
|                             | CLK             | GPIO 18                     |
| **LED Matrix Module 2**     | DIN (from DOUT) | Matrix 1 **DOUT**           |
|                             | VCC             | 3.3V                        |
|                             | GND             | GND                         |
| **Micro Servo 1 (SG90)**     | VCC             | Step Down **OUT+**          |
|                             | GND             | GND                         |
|                             | Signal          | GPIO 13                     |
| **Micro Servo 2**           | Signal          | GPIO 12                     |
| **Micro Servo 3**           | Signal          | GPIO 14                     |
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
1. **Ground Connections**: Ensure all components share a **common ground** for proper operation.
2. **Power Supply**: Use the Step-Down Module to provide a steady 5V for servos and PAM8403, and 3.3V for the ESP32 and LED matrices.

## Bill of Components

| Quantity | Material                                   | Link to shop  										                                                                         | Datasheet     |
|----------|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
|    1     | ESP32-WROOM-32D                            | [SHOP LINK](https://www.sigmanortec.ro/placa-dezvoltare-esp32-cu-wifi-si-bluetooth)   										 | [DATASHEET](file:///C:/Users/anama/Downloads/esp32-wroom-32d_esp32-wroom-32u_datasheet_en.pdf) |
|    2     | LED Matrix Module MAX7219                  | [SHOP LINK](https://www.optimusdigital.ro/ro/optoelectronice-matrice-de-led-uri/118-modul-cu-matrice-de-led-uri-max7219.html?search_query=matrice+led&results=51)      | [DATASHEET](file:///C:/Users/anama/AppData/Local/Microsoft/Windows/INetCache/IE/D0JNYWEH/MAX7219-Datasheet[1].pdf) |
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
