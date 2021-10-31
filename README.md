# EmSys: Synchronous Sequential Logic

In the previous lecture, we explored how to design logic circuits using the Verilog hardware description language. All the circuits we designed were combinatorial; these are circuits where the output depends solely on the current inputs. However, most circuits, such as CPUs, require the storage of state. Storing state means that the circuit depends on both the current inputs and the history of the device's execution.

Saving state introduces an extra layer of complexity when designing circuits, __synchronisation__. For combinatorial circuits, when the input changes, the effects are propagated through the circuit. However, these changes do not take place instantaneously but are subject to some delay. The time it takes the signal to propagate through gates and wires means that when the input changes it can take a time before the output changes.

To store state in the system, we essentially need to create a feedback loop in our circuit. Where data that is produced in previous iterations is taken from the output and sent back to the input. As the data is flowing back through the circuit, we have some memory of the output. 
