# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that lacks proper overflow handling. The `buggy_counter.vhd` file contains the erroneous code, while `fixed_counter.vhd` provides a corrected version.

The bug is caused by the counter incrementing without a check for reaching the maximum value. This can lead to unpredictable behavior in simulation and hardware implementation.  The corrected code addresses this by adding a check to wrap the counter back to 0 when the maximum value is reached.

## How to Reproduce

1.  Simulate `buggy_counter.vhd` using a VHDL simulator (e.g., ModelSim, GHDL). Observe the counter behavior when it exceeds 15.
2.  Simulate `fixed_counter.vhd` to see the corrected behavior.

## Bug Fix

The solution involves adding a modulo operator to ensure the counter wraps around correctly when it reaches the maximum count.
