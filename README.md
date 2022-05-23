# Universalshift Register using LTSpice
LTspice is a simulation software that is used to simulate the  circuits
you can download the LTspice from [here](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
### Introduction
A register that can store the data and /shifts the data towards the right and left along with
the parallel load capability is known as a universal shift register. It can be used to perform
input/output operations in both serial and parallel modes. Unidirectional shift registers and
bidirectional shift registers are combined to get the design of the universal shift register. It is
also known as a parallel-in-parallel-out shift register or shift register with the parallel load.
Universal shift registers can perform 3 operations as listed below <br />
• Parallel load operation – stores the data in parallel as well as the data in parallel<br />
• Shift left operation – stores the data and transfers the data shifting towards left in the
serial path<br />
• Shift right operation – stores the data and transfers the data by shifting towards right
in the serial path.<br />

![](https://i.imgur.com/EAbFlbd.png)
### Explanation:
• Serial input for shift-right control enables the data transfer towards the right and all the
serial input and output lines are connected to the shift-right mode. The input is given to
the AND gate-1 of the flip-flop -1 as shown in the figure via serial input pin.<br/>
• Serial input for shift-left enables the data transfer towards the left and all the serial
input and output lines are connected to shift-left mode.<br/>
• In parallel data transfer, all the parallel inputs and outputs lines are associated with the
parallel load.<br/>
• Clear pin clears the register and set to 0.<br/>
• CLK pin provides clock pulses to synchronize all the operations.<br/>
• In the control state, the information or data in the register would not change even
though the clock pulse is applied.<br/>
• If the register operates with a parallel load and shifts the data towards the right and left,
then it acts as a universal shift register.<br/>
### Universal Shift Register Working
• From the above figure, selected pins the mode of operation of the universal shift
register. Serial input shifts the data towards the right and left and stores the data within
the register.<br/>
• Clear pin and CLK pin are connected to the flip-flop.
• M0, M1, M2, M3 are the parallel inputs while F0, F1, F2, F3 are the parallel outputs of
flip-flops<br/>
• When the input pin is active HIGH, then the universal shift register loads / retrieve the
data in parallel. In this case, the input pin is directly connected to 4×1 MUX<br/>
• When the input pin (mode) is active LOW, then the universal shift register shifts the
data. In this case, the input pin is connected to 4×1 MUX via NOT gate.<br/>
• When the input pin (mode) is connected to GND (Ground), then the universal shift
registers act as a Bi-directional shift register.<br/>
• To perform the shift-right operation, the input pin is fed to the 1st AND gate of the 1st
flip-flop via serial input for shit-right.<br/>
• To perform the shift-left operation, the input pin is fed to the 8th AND gate of the last
flip-flop via input M.<br/>
• If the selected pins S0= 0 and S1 = 0, then this register does not operate in any mode.<br/>
That means it will be in a Locked state or no change state even though the clock pulses
are applied.<br/>
• If the selected pins S0 = 0 and S1 = 1, then this register transfers or shifts the data to left
and stores the data.<br/>
• If the selected pins S0 = 1 and S1 = 0, then this register shifts the data to right and hence
performs the shift-right operation.<br/>
• If the selected pins S0 = 1 and S1 = 1, then this register loads the data in parallel. Hence
it performs the parallel loading operation and stores the data.<br/>

| S0    | S1    | Mode of Operation |
| :---: | :---: | :---: |
| 0     | 0     |  Locked state (No change)|
| 0     | 1     | Shift-Left|
| 1     | 0     | Shift-Right|
| 1     | 1     | Parallel loading|
### Instructions to runcode:
First copy the Tsmc018.lib in library files in (your LT spice installed libray)/lib/sub<br/>
Now copy cmosp and cmosn in (your LT spice installed libray)/lib/sym <br/>
Run file TESTBENCH.asc to get results <br/>
then you are good to go <br/>



Authour:K Kiran Reddy<br/>
Refered from various internet sources

