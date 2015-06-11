#C88 computer Javascript emulator

This ia an emulator for the C88 computer.

A minimalist CPU architecture with only 64 bits of memory.

It is implemented in an FPGA using VHDL, it is available here: https://github.com/danieljabailey/C88

This is an emulator for that machine, implemented in javascript.

##Usage

Just open up the c88.html file and enter a program by clicking on the memory bits to toggle them.

Run the program with the run and step buttons at the bottom.

The reset button will set the PC and main register to zero.

##Library

c88.js is a file containing the emulator without the GUI.
You can use this to make your own gui.

First get a c88 object like this:

```
	c = new c88();
```

Then you can set the memory which is an array of eight integers:
```
	c.mem=[224, 37, 6, 23, 64, 7, 1, 0];
```

Then run the program and update some kind of memory display:
```
	setInterval(
		function(){
			c.step();
			myDisplay = c.mem;
		},1);
```
