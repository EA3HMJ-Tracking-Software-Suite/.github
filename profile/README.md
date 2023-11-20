# Welcome to EA3HMJ Tracking Software Suite
![ECOSISTEMA_v4](https://github.com/EA3HMJ-Tracking-Software-Suite/.github/assets/2368602/c14ddea2-012e-4957-8e9b-9935d09bc365)
## Description
This is an antenna tracking system that integrates dedicated hardware and software designed for amateur use in Earth–Moon–Earth communication (EME), radioastronomy, amateur Deep Sky Network (DSN) and other Space Communications applications where accurate and high precision tracking are required. 
Proper use of the system requires electronics knowledge and some software skills. Thus, it is only recommended to users with previous experience with antenna tracking systems.

The hardware components of this system are specifically selected to support the software applications that run on it. These components include a DishController unit -including a ESP32 microcontroller unit (MCU), DC or AC motor driver board with high-performance and high-current driver devices, RS485 input/output devices and DC voltage step-up converter-, other peripherals like a variety of absolute digital encoders and inclinometers to sense the motion and position of the motorized slewing drive system and a remote-control unit.

In order to support single-turn and multiturn absolute encoders with parallel output interface there is also an optional Parallel to RS485 MODBUS converter board. Obviously, the latter is not needed if the sensors outputs are Modbus RS485 compliant.

The software components of this system are also specifically designed to work with the hardware components. This software includes the microcontroller and remote-control firmware, communications protocol, device drivers, and application software. 

The DishController MCU firmware controls and monitors the operation of the slewing drive motors, azimuth encoders, and elevation inclinometers.

The application software includes the DriverDish program, which is responsible for requesting data from the ephemeris server and communicating with the DishController unit, and a suite of server programs (JPLastroserver, Astroserver and Astronomyserver) that obtain the most accurate positioning data that is feasible and available from trustworthy sources. 

The integration of dedicated hardware and software in such a system provides several benefits. First, it improves system performance and reliability by allowing the DishController unit to directly access and control the specialized hardware components like the motor drivers and position sensors. This reduces overhead and improve response times. Second, it simplifies system design and development by providing a standardized set of hardware and software components that are optimized for narrow beamwidth antenna tracking. Third, in contrast to other antenna tracking system designs, the movement and position sensors are located at the last link of the movement chain to actively monitor the antenna's pointing direction. By doing so, the system is able to minimize the impact of mechanical tolerances and gear backslash.

The system is made up of blocks that are interlinked with each other:
- Ephemerides servers
  - [Astroserver](https://github.com/EA3HMJ-Tracking-Software-Suit/Astroserver)
  - [JPLastroserver](https://github.com/EA3HMJ-Tracking-Software-Suit/JPLastroserver)
  - [Astronomyserver](https://github.com/EA3HMJ-Tracking-Software-Suit/Astronomyserver)
- Control application in Windows OS
  - [DriverDish](https://github.com/EA3HMJ-Tracking-Software-Suit/DriverDish)
  - [SN server](https://github.com/EA3HMJ-Tracking-Software-Suit/SNserver)
- Antenna Controller
  - [Controller Dish](https://github.com/EA3HMJ-Tracking-Software-Suit/ControllerDish)
  - [Mini weather station](https://github.com/EA3HMJ-Tracking-Software-Suit/MiniWx)
  - [Remote control](https://github.com/EA3HMJ-Tracking-Software-Suit/RemoteControl)
  - [Interface encoder paralell to RS485](https://github.com/EA3HMJ-Tracking-Software-Suit/Paralell-Interface)
  - [Interface encoder USdigital A2 to RS485](https://github.com/EA3HMJ-Tracking-Software-Suit/A2-Interface)
- Utilities
  - [Heatmap](https://github.com/EA3HMJ-Tracking-Software-Suit/Heatmap)

## Starting
The following document explains how to start the system:

- [Getting Started Guide ENG](https://github.com/EA3HMJ-Tracking-Software-Suit/.github/blob/main/Star%20up%20tracking%20system%20v1%20ENG.pdf)
- [Guia ESP](https://github.com/EA3HMJ-Tracking-Software-Suit/.github/blob/main/Star%20up%20tracking%20system%20v1%20ESP.pdf)


## Project support
I dedicate a substantial portion of my free time to the development of the “EA3HMJ Tracking Software Suite” project, and I take great satisfaction in its progress. I believe it serves as a relevant contribution to the Ham Radio and Amateur DSN, communities offering an opportunity to establish a state-of the-art high-precision tracking system at an affordable cost.

However, beyond the investments of time and effort, there are tangible expenses involved, such as purchasing components, PCB fabrication, acquiring tools, and obtaining new sensors. These ancillary expenditures are crucial to ensuring the creation of a robust system at an affordable price point.

If you would like to support the ongoing maintenance of this software-hardware ecosystem through a donation, you can do it through my paypal 'qlfecv'+'@'+'gmail'+'.'+'com'. 

## Disclaimer
This software -including the source and the whole package- and hardware are distributed "as is" without any representation or warranty of any kind, either express or implied. 

Please note that I am not able to provide support for this antenna tracking system. I designed and wrote it for myself and I am willing to share it here for those asking about my tracking system. I do not guarantee the accuracy or completeness of the information and materials distributed here. The software source has been tested on a real environment and scanned for viruses and has passed all tests.

I shall not be liable for any errors or omissions and shall not be responsible for any damages arising from the use of this antenna tracking system. I shall not be held responsible for any issues or problems that may arise from the use of it. 
By using any part of this antenna tracking system (software or hardware), you acknowledge and agree to the terms of this disclaimer.
