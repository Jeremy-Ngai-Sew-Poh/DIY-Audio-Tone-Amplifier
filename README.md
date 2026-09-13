# DIY Desk Audio Amplifier with Tone Control & Dual Input
This is a desk audio amplifier I designed and built to quickly switch between 2 audio sources and apply custom analogue Baxandall EQ to audio without software dependency. It is capable of delivering a maximum of 2x5W output compatible with 4 ohm and 8 ohm speakers.

![Hero Image](https://github.com/Jeremy-Ngai-Sew-Poh/DIY-Audio-Tone-Amplifier/blob/main/images/Hero%20Image.jpg)

## Background
I was frustrated when switching speaker input between my pc and my piano keyboard because I had to move my pc off my desk just to unplug the audio cable from the chassis and plug it back in after my piano practice multiple times a day. That time, I was using my PAM8403 module with the audio cable directly soldered onboard. So, the audio cable cannot be unplugged on the module end. 

A while after that, I decided to make another amplifier board upgraded with removable audio jack connector onboard to make my life easier. However, just as I thought it would finally be over, the module came faulty.. Total waste of time.

This is why I came up with this _over-engineered_ audio amplifier that lets me switch 2 audio sources with just a switch and lets me control EQ without software.

## Overall Design
### Power Input
The build is powered with 5V input via USB Type-C and through a toggle switch to control power. It also works with PD negotiation with a pull-down resistor on CC lines.

### Audio Input
Allows 2 distinct audio sources to be quickly switched with a DPDT toggle switch without unplugging/replugging audio jacks. It is compatible with TRRS and TRS connectors

### Audio Tone Control
The build uses a passive 2 channel Baxandall tone control circuit to alter bass and treble frequencies before reaching the main amplifier module. This introduces an insertion loss of around 20dB.

* Bass Turnover Frequency ($f_c$): ~72Hz
* Treble Turnover Frequency ($f_c$): ~7.2kHz

### Amplification
The amplifier system is powered by the HT8696 Class D/AB stereo ready-made module capable of outputting ~10W at 5V with anti-clipping capability to reduce buzzing issues.

## Repository Structure
* `easyeda/`: Schematics and PCB layout in EasyEDA Pro format.
* `cad/`: 3D STL files.
* `images/`: Project images.

## Bill Of Materials (BOM)

|Reference| Component | Variation | Quantity | Link |
|--------| -------- | -------- | -------- | -------- |
|U1| HT8696 Module | 10W | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c45hUW2p) |
|U4| Type-C Connector | 6 Pin | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c3UOzwXl) |
|SW1| MTS-102 Toggle Switch | SPDT ON-ON | 1 | [AliExpress](https://s.click.aliexpress.com/e/_c3D1ScVt) |
|SW2, SW3| MTS-202 Toggle Switch | DPDT ON-ON | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c33nnhHl) |
|U2, U3| PJ320D 3.5mm Jack | SMT | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c2RY3vNl) |
|U5, U6| KF301 Screw Terminal | 2 Pin | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c3UOZrux) |
|VR1 - VR4| Slide Potentiometer | B100K, 75mm Length, 15mm Lever | 4 | [AliExpress](https://s.click.aliexpress.com/e/_c4K0umGf) |
|R1, R2| 0805 Resistor | 5.1K | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
|R3 - R8| 0805 Resistor | 10K | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
|R9 - R14| 0805 Resistor | 510 | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c4FGkatZ) |
|C3, C7| 0805 Capacitor | 2.2nF | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
|C1, C4, C5, C8| 0805 Capacitor | 22nF | 4 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
|C2, C6| 0805 Capacitor | 220nF | 2 | [AliExpress](https://s.click.aliexpress.com/e/_c38nTHDd) |
|LED1 - LED6| 0805 LED | Warm White | 6 | [AliExpress](https://s.click.aliexpress.com/e/_c3y6gdeJ) |

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

## License
This project is licensed under the GNU General Public License v2.0.
