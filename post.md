# Lab X: Doing stuff with hardware!

## Overview and Motivation - Utsav
This week we'll explore...




## 2 to 1 Multiplexer - Long
### Objective
In this first part of the lab, we will simulate a 2 to 1 multiplexer using only AND, OR and NOT gates. The aim here is to demonstrate that any multiplexer can be taken apart into basic Boolean logic. By using just AND, OR, and NOT gates, we can create all kinds of multiplexers, like 2 to 1 or 16 to 1.
### Materials
The materials required for this part are: one circuit diagram, one wiring diagram, a PB-503 breadboard, as well as 3 IC chips: 7404 (NOT), 7408 (AND), and 7432 (OR). 

<center><img src="images/2to1Wiring.png" width="350" height="500"></center>

<center>2 to 1 wiring diagram</center>

<center><img src="images/2to1Circuit.png" width="400" height="600"></center>

<center>2 to 1 circuit diagram</center>


### Steps 

    Step 1: We wire the 5 volts source to the top row of the breadboard, as well as the ground to the row right below.

    Step 2: We plug two AND chips, one NOT chips, and one OR chips into the breadboard. We connect the IC chips' VCC into the 5 volts source and GND into the ground.

    Step 3: The S1 switch is going to be our select line for the multiplexer, with the S5 switch representing input line A and the S6 switch representing input line B. We connect S1 and S6 to an AND gate's input pins (1A and 1B). 

    Step 4: We also connect S1 to an inverter (NOT gate), through which the signal from S1 will be inverted and directed to the other AND gate's input pin. This AND gate also takes signal from S5.

    Step 5: The output from our two AND gates will be connected to our OR gate, whose input is wired to the logic probe (the red and green indicator light on our breadboard).

Our breadboard would look like this:
 
<center><img src="images/2to1Construction.jpg" width="400" height="600"></center>

<center>2 to 1 circuit</center>

### Testing 
Testing this circuit board is simple. From the wiring diagram, we see that depending on the signal from S1, the output to the OR gate would come from either the top or bottom AND gate. If S1 sends a 1, then output will be dependent on the S6 switch. Otherwise, if S1 sends a 0, the signal goes through the inverter, where it is turned to 1, activating the top AND gate. The output will now depends on S5. This testing procedure can be shown in the video below.





## 4 to 1 Multiplexer - Long
### Objective

The goal of this section is to get us familiarity with the 74150 chip, which is a 16 to 1 multiplexer. We will only build a 4 to 1 multiplexer using this chip, which means only 4 out of the 16 data lines and 2 out of the 4 input lines will be used.

### Materials
We will need a 74150 16 to 1 multiplexer chip, its documentation with the function table for configuring data selects, a wiring diagram, and the PB-503 breadboard.

### Steps 
We will do the wirings based on the wiring diagram below.

<center><img src="images/4to1Diagram.png" width="600" height="500"></center>

<center>4 to 1 multiplexer diagram</center>

    Step 1: We plug in the multiplexer chip into the breadboard, connecting it to the 5 volts power source and ground using its VCC and GND pins, respectively.

    Step 2: The strobe - the bottom 4th pin from the right - must always be connected to the ground, otherwise the multiplexer will not output anything. The output pin on the right of the strobe is wired to our logic probe.

    Step 3: We connect the chip's select lines A and B (top 3rd and 2nd pins from the right) to switch S1 and S2. Select lines C and D will always be wired to the ground, since the data lines we are using all require C's and D's signal to be 0. The chip's data lines E0 (left of the strobe), E1, E2, and E3 are connected to switch S5, S6, S7, S8.

After these steps, our breadboard will look like this: 

<center><img src="images/4to1Mux.jpg" width="500" height="700"></center>

<center>4 to 1 multiplexer</center>


### Testing

To test that the multiplexer works as expected, we rely on its function board. If the combination of select lines allow the desired inputs line to work, then the multiplexer is behaving correctly. Looking at the function table, E0, E1, E2, and E3 all require C and D to be 0, which is why we connect them to the ground instead of a switch. We test the following: 

    - when A and B are low, input line E0 works.
    - when A is high and B is low, input line E1 works.
    - when A is low and B is high, input line E2 works.
    - when A and B are high, input line E3 works.

Our testing is demonstrated in the video below.

## 4 to 1 Multiplexer with Arduino - Vuong
### Objective

### Materials 

### Steps 

### Testing 





## Adder - Vuong
### Objective

### Materials

### Steps

### Testing





## Conclusion - Utsav




