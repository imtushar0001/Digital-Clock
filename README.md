# Digital Clock Project

## Overview
This project involves the design and implementation of a digital clock on the Basys-3 FPGA board using Icarus Verilog (iverilog) for synthesis and GTKWave for simulation. The clock supports four distinct features: a 24-hour clock, alarm, timer, and stopwatch.

## Features
- *24-Hour Clock*: Displays time in 24-hour format.
- *Alarm*: Allows setting an alarm which alerts when the set time is reached.
- *Timer*: Functions as a countdown timer.
- *Stopwatch*: Measures elapsed time from a starting point.

## Project Structure
The project includes the following files:
- *basys3.xdc*: Constraint file for the Basys-3 FPGA board.
- *clk.v*: Module for clock signal generation.
- *clkDivider.v*: Module for clock signal division to achieve different timing requirements.

## Getting Started
To replicate this project, follow the steps below:

### Prerequisites
- Basys-3 FPGA Board
- Icarus Verilog (iverilog)
- GTKWave

### Cloning the Repository
bash
*git clone (https://github.com/imtushar0001/Digital-Clock)*

*cd Digital-Clock*


### Simulation and Synthesis
1. *Simulation*: Use Icarus Verilog to simulate the design.
   bash
   iverilog -o clock_tb clk.v clkDivider.v
   vvp clock_tb
   gtkwave clock_tb.vcd
   
2. *Synthesis*: Use Vivado for synthesis and upload to Basys-3 FPGA board.
   - Open Vivado and create a new project.
   - Add the clk.v and clkDivider.v files to the project.
   - Add the basys3.xdc constraint file.
   - Run synthesis, implementation, and generate the bitstream.
   - Upload the bitstream to the Basys-3 FPGA board.

## Usage
- *24-Hour Clock*: The main display shows the current time in 24-hour format.
- *Alarm*: Set the alarm time using the designated input switches/buttons. The alarm will trigger at the set time.
- *Timer*: Set the countdown duration and start the timer.
- *Stopwatch*: Start and stop the stopwatch to measure elapsed time.

## Contributing
Feel free to fork this project and contribute by submitting pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Dr. Srinivas Boppu for guidance and support.
