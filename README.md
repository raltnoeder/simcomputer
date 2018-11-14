# The simcomputer project

This project contains a simple 16 bit/word-addressed [harvard architecture](https://en.wikipedia.org/wiki/Harvard_architecture) [CISC](https://en.wikipedia.org/wiki/Complex_instruction_set_computer) computer built as a circuit for the [Logisim](http://www.cburch.com/logisim/) logic circuit simulator, along with some programs that can be loaded into the simulated computer's program memory and can then be run on the simulated computer.

## What is it good for?
- It can be used to gain insight into how a computer works
- It can help you learn how to manually code machine instructions
- It's a cool toy for geeks

## Simulated computer overview
- 128 kiB word-addressed (16 bit) RAM
- 128 kiB word-addressed (16 bit) read-only program memory
- 7 general purpose 16 bit registers
- 18 instructions
- 60 x 15 text output terminal

This simulated computer is about as powerful as 1950s computers like the Harvard Mark III

## Documentation
There is some documentation of the instruction set available, although it still describes the predecessor B1601 processor design, while the simulated computer available in the project uses the newer B1602 processor design. The B1602 is compatible with the B1601, but some new capabilities are not documented in the B1601 instruction set documentation.

## How to use the simulated computer

- Download and run [Logisim](http://www.cburch.com/logisim/)
- Download this project and load the simcomputer.circ file into Logisim
- You should now see the simcomputer circuit
- Select the hand tool in Logisim (it's normally in the upper left corner)
- Click on the simcomputer component labeled "PROGRAM ROM"
- Double click the lens icon that appeared on it
- You should now see two small boxes connected to a large box in the middle
- Right click the large box in the middle
- Select "Load image" from the menu
- Load one of the programs from the "programs" subdirectory of this project
- In the Logisim menu, select Simulate > Go out to state > sysboard
- You should see the simcomputer circuit again
- In the Logisim menu, select Simulate > Simulation enabled
- Select Simulate > Reset simulation
- Select Simulate > Ticks enabled (make sure it's checked)
- Make sure you still have the Logisim hand tool selected
- On the simcomputer control panel to the right, click the button labeled "RESET"
- The LED labeled "INSTR READY" should now be on
- On the control panel, click "RUN"
- The LED labeled "RUN ENBL" and "PROC" should now be on and the program should start running

There is a program file named "systest.img", it is a good idea to try running this program first.
It tests all instructions and if it is able to finish, it will confirm that the simcomputer is operating correctly.

