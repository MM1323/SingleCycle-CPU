# SingleCycle-CPU
Purpose: Putting different components together to create a single cycle ARMv8 (simplified) CPU

The ARMv8 instructions implemented: add, sub, and, or, ldur, stur, cbz, b

1. Complete the control circuits to implement all the instructions given in the file controls.docx (completed for
homework), controls.pdf. Do this by completing the two subcircuits: ALUControl_0 and Control_0. (The
circuits ALUControl and Control use these.) Save the file.
Note: the order of the control outputs is not the same as in the book diagrams. See the filespecs.
Hint1: Compare the opcodes and determine how many of the bits are needed (2, 3, 4, 5, ?) to
differentiate each instruction or class (R-type). Use those lines to set the appropriate bits for the
output.

2. Open your SingleCycleCPU.circ. Click on the control subcircuit to check that your implemented version has
been loaded. Delete the controls in the circuit (these should have been the fake-controls) and then add
ALUControl and Control from the new circuits instead.

3. Test your circuit by running the test program. Load test.mem and testdata.mem as in part 1, then click on the
clock icon repeatedly to execute the program. (You do not have to enter control values by hand, of course.) You
should get the behavior described in part 1.

4. Now try the program arraysum.s It finds the partial sums of the array, storing them back into the array, so
when done the kth item in the array is the sum of the first k values in the original array. Load arraysum.mem and
arraysumdata.mem into the instruction and data memories, then run the program.
When you are tired of clicking the clock icon, you can set the frequency of ticks under the simulate menu, then
click "ticks enabled" and the clock will run by itself, until you uncheck "ticks enabled".

6. When the program completes (by cycling forever on the last instruction), the data memory should contain the
following:
00 00000003
01 00000012
02 00000026
03 00000028

Sometimes the simulator has a hiccup and does not save the proper value. If you think your circuit is correct and
you get a glitch in the results, try again by reloading the data memory and resetting the circuit (click reset twice).
