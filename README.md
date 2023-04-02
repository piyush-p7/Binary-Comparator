# Binary Comparator Verilog Module
This Verilog module implements a binary comparator that compares two 64-bit binary numbers and determines whether they are greater than, less than, or equal to each other. The module has four output signals that indicate the comparison result: greater, smaller, equal, and invalid.

The comparison algorithm used in this module is based on a binary tree. The difference between the two input numbers is computed using a wire called diff, and the result of the comparison is computed using a 6-bit signal called result.

The module has two always blocks. The first always block implements the binary tree comparison algorithm, and the second always block outputs the comparison result based on the result signal. There is also an initial block in the testbench module that provides stimulus to the comparator and displays the output signals.

To use this module, instantiate it in your Verilog design and connect the input and output signals. The dataA and dataB inputs are the two numbers to be compared, and the greater, smaller, equal, and invalid outputs indicate the comparison result.

# Usage
Instantiate the module in your Verilog design and connect the input and output signals:
```
verilog
Copy code
binaryComparator comparator (
    .dataA(dataA),
    .dataB(dataB),
    .greater(greater),
    .smaller(smaller),
    .invalid(invalid),
    .equal(equal)
);
```
- dataA: 64-bit input signal representing the first number to be compared
- dataB: 64-bit input signal representing the second number to be compared
- greater: output signal indicating whether dataA is greater than dataB
- smaller: output signal indicating whether dataA is smaller than dataB
- invalid: output signal indicating whether the comparison result is invalid (e.g., due to overflow or underflow)
- equal: output signal indicating whether dataA is equal to dataB
# License
This Verilog module is released under the MIT License. See the LICENSE file for more information.

# Acknowledgements
This module was created by Piyush Pandita for Digital Designs course at Vishwakarma Institute of Technology, Pune, INDIA.
