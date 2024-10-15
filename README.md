# NI-DAQmx Digital I/O Control

**NI-DAQmx Digital I/O Control** is a LabVIEW application that manages digital input and output operations using National Instruments hardware with NI-DAQmx. The program is split into two main sections, represented by separate virtual instruments (VIs): `In.vi` for digital input and `Out.vi` for digital output.

## Features:
- **Digital Input (`In.vi`)**: 
  - Reads digital boolean values from a specified digital input line.
  - The data is processed sequentially, performing operations based on digital state changes.
  - Each input state is passed through a series of logic steps and conditions to manipulate the output.
  
- **Digital Output (`Out.vi`)**: 
  - Sends digital boolean signals to a specified digital output line.
  - Continuously monitors the output state and updates based on logic conditions.
  - Displays the result of the current state of the digital output in real time.

## How It Works:
1. **In.vi (Digital Input)**:
   - Configures and reads from a digital input line (`Dev1/port0/line0`).
   - Processes the input and performs logical operations (e.g., toggling states, conditional checking).
   - Outputs the result of the logic to corresponding digital output lines.
   
2. **Out.vi (Digital Output)**:
   - Sends digital signals to the output lines (`Dev1/port0/line0` and `Dev1/port1/line0`).
   - Monitors the digital output status and displays real-time results of the output states.
   - Provides a safe way to stop the program through a stop button.

## Requirements:
- LabVIEW
- NI-DAQmx Driver installed
- National Instruments hardware supporting digital I/O operations

## Usage:
1. Configure the digital input and output channels on your NI device.
2. Run `In.vi` to monitor and process digital input states.
3. Run `Out.vi` to send and monitor digital output states.
4. Use the stop button in `Out.vi` to safely stop the program.

## Example:
- In `In.vi`, the digital input is read from `Dev1/port0/line0`, processed through a sequence of boolean conditions, and passed to different output channels.
- In `Out.vi`, digital output is sent through two separate channels and displayed for monitoring.

Ensure that NI-DAQmx is correctly installed and your device is properly configured before running the VIs.

## Code:
### In.vi
![image](https://github.com/user-attachments/assets/2867aa29-2799-4b42-b026-a53dffcda394)
### Out.vi
![image](https://github.com/user-attachments/assets/aa2a73e0-2148-4e75-93ae-94286c84aeae)
