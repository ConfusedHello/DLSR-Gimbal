# DSLR Gimbal
A DIY 3-axis camera gimbal designed for full frame cameras, built as part of the Hack Club Highway to Hardware program!

As I'm somewhat of a hobbyist photographer, I've considered the idea of building my own camera gimbal for videography as even second-hand on Facebook Marketplace they can be a few hundred AUD. However, I've never particularly had the opportunity (or funds) to attempt it ~~spent all my money on cameras~~.

The gimbal is is powered by iPower's GM5208-24 brushless motors and is constructed primarily from Carbon Fibre sheets/tubes.

<!-- At the time of building, the project cost AU$ , or approx. US$ . -->

For details about the design process, other information, check out the [development journal](highway.hackclub.com/projects/ConfusedHello/DLSR-Gimbal). \*Local copy available in [JOURNAL.md](/JOURNAL.md)

The BOM for the frame is in [/src/frame/README.md](/src/frame/README.md) while the BOM for the PCBs are in [/production/BOM](https://github.com/ConfusedHello/STorM32-NT/). For simplicity, a summary has been provided at the bottom of this document.

## The Frame:
![Frame](/assets/Frame_Prog3.png) 

## The Controller
![PCB](/assets/Panel.png)

## The Setup
![Diagram](/assets/Gimbal_Layout_Initial.png)
![Diagram](/assets/Gimbal_Layout_Wiring_Initial.png)

## BOM
### Frame
| Item Name                           | Cost (Total) | Amount | Link|
|-------------------------------------|--------------|--------|----|
| GM5208-24 motor                     | AU$207.75    | 3      | [Aliexpress](https://www.aliexpress.com/item/32900557812.html) |
| 200x300x3mm Carbon Fibre Panel      | AU$80.07     | 3      | [Aliexpress](https://www.aliexpress.com/item/1005007049758967.html) |
| 22x20x600mm Carbon Fibre tube (2pc) | AU$60.99     | 2      | [Aliexpress](www.aliexpress.com/item/1005006421809160.html) |
| Aluminium Tube Clamp                | AU$74.80     | 44     | [Aliexpress](https://www.aliexpress.com/item/1005001563658390.html) |
| Camera Screw                        | AU$2.14      | 1      | [Aliexpress](https://www.aliexpress.com/item/1005006636367450.html) |
Total price: AUD$425.75 (approx. USD$276.34)

### PCB and Components
| Item Name | Cost (Total) | Amount | Link |
|---|---|---|---|
| STM32G431KBU3 | $6.9561 | 3 | [https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32G431KBU3_C1341901.html](https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32G431KBU3_C1341901.html) |
| STM32F103RCT6 | $1.89 | 1 | [https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32F103RCT6_C8323.html](https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32F103RCT6_C8323.html) |
| STM32F103T8U6 | $3.16 | 1 | [https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32F103T8U6_C19671.html](https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32F103T8U6_C19671.html) |
| Misc. Components (Resistors, Capacitors, Sockets, IMU, V-reg) | ~$40 | | |
|PCB	|A$3.08	|1	||
|Stencil	|A$10.77|	1	||
| Shipping	|A$26.21|	1||

Combined total for the project:
AUD$425.75 + USD$25.97 + USD$52
= approx. USD$326.12


<hr>

Made with ❤️ by [@ConfusedHello](https://github.com/confusedhello)
