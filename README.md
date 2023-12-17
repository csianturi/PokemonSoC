# PokemonSoC
This project involves the building of a SoC and implementing on a Nexys A7-100T FPGA. The SoC itself uses a MicroBlaze MCS system with an MMIO and video subsystem
## MMIO Subsystem
The MMIO subsystem consists of a controller to select a specific slot and can accommodate up to 64 instantiated cores. After being “wrapped” with an interface circuit, custom digital logic can be plugged into the FPGA platform. I used a number of these cores to implement things such as UART, I2C, SPI, PS2 keyboard/mouse input, GPIO, timers, PWM, and ADCs to connect outside components.
## Video Subsystem
The video subsystem establishes a framework to coordinate the operation of video cores. A video core generates or processes the video data stream. The cores are arranged as a cascading chain. The data stream is pipelined and “blended” through each stage and eventually displayed on a VGA monitor. The video subsystem demonstrates the principles of handling stream data, in which data are generated continuously and passed through a chain of components for processing.
## Final Result
![Title Screen Picture](PokemonSoc/Images/titlescreen.jpg)
![Game Screen Picture](PokemonSoc/Images/pokemongame.jpg)
