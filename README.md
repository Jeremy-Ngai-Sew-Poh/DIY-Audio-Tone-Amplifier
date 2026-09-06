# DIY Audio Amplifier with Tone Control & Dual Input

## Background

## Features

## Repository Structure
* `easyeda/`: Schematics and PCB layout in EasyEDA Pro format.
* `cad/`: 3D STL files.
* `image/`: Project images.

## Bill Of Materials (BOM)

| Component | Variation | Quantity | Link |
| -------- | -------- | -------- | -------- |
| HT8696 Module | 10W | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c3eED1G7) |
| Type-C Connector | 6 Pin | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c3UOzwXl) |
| MTS-102 Toggle Switch | SPDT ON-ON | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c3D1ScVt) |
| MTS-202 Toggle Switch | DPDT ON-ON | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c33nnhHl) |
| PJ320D 3.5mm Jack | SMT | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c2RY3vNl) |
| KF301 Screw Terminal | 2 Pin | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c3UOZrux) |
| Slide Potentiometer | B100K, 75mm Length, 15mm Lever | 4 | [AliExpress](https://s.click.aliexpress.com/e/_c4K0umGf) |
| 0805 Resistor | 5.1K | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
| 0805 Resistor | 10K | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
| 0805 Resistor | 510 | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
| 0805 Capacitor | 2.2nF | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
| 0805 Capacitor | 22nF | 4 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
| 0805 Capacitor | 220nF | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
| 0805 LED | Warm White | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c3y6gdeJ) |

## PCB Schematics
![PCB Schematics](https://github.com/Jeremy-Ngai-Sew-Poh/DIY-Audio-Tone-Amplifier/blob/main/images/PCB%20Schematics%20v1.1.png)

## PCB Layout
Top:

![PCB Layout Top](https://github.com/Jeremy-Ngai-Sew-Poh/DIY-Audio-Tone-Amplifier/blob/main/images/PCB%20Layout%20Top%20v1.1.png)

Bottom:

![PCB Layout Bottom](https://github.com/Jeremy-Ngai-Sew-Poh/DIY-Audio-Tone-Amplifier/blob/main/images/PCB%20Layout%20Bottom%20v1.1.png)

## Revisions
* **V1.0**: Initial prototype. Mismatched ground plane between `JACK_GND` and common ground, require solder bridge fix. 
* **V1.1**: Fixed ground plane net and routing. Working as it should! 

