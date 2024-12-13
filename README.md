# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL: counter overflow.  The `buggy_counter.vhdl` file contains a counter that increments without checking for the upper bound of its range.  This can lead to unexpected behavior or simulation failures.

The solution, `fixed_counter.vhdl`, addresses this by explicitly handling the overflow condition. This example highlights the importance of careful range checking in VHDL designs to prevent unexpected behavior.

## Bug Description

The buggy code increments the counter without checking whether it has reached the maximum value (15).  Once the counter reaches 15, the next increment will result in an overflow, potentially causing the counter to wrap around to 0 or produce unpredictable results. 

## Solution

The corrected code in `fixed_counter.vhdl` includes a conditional statement to prevent the overflow.  When the counter reaches the maximum value, it remains at the maximum value instead of incrementing further.