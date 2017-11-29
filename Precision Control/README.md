# Lab 6: Precision Control

## PWM Part 2
The code for the PWM was implemented using a hardware approach. Using one CCR to determine the frequency and another to determine the duty cycle, a PWM signal could be output to a pin. The PWM then was able to convert a digital voltage into an analog reading. This analog voltage could then be read from the pin that the PWM is output to. To test this code a triangle wave was coded and then implemented to see the range of voltages that the PWM could output. The triangle wave produced by the PWM can be seen below compared to a similar wave produced by a function generator
 
FIGURE

## R2R DAC
To implement the R2R DAC, the circuit seen below was used. 

FIGURE

This circuit was able to take individual bits of a digital signal at each node of the circuit and then output an equivalent analog voltage. Since there is 8 nodes on the circuit the digital signal could vary from varied from 0-255. In a different bit of a digital volatge signa was putput to an independent pin by masking the desired signal 8 different times to save the value of each bit into a separate variable. These varaible were called bit0-bit7 and represented their respective bit of the digital signal. The variables were then ouptut to pins and connected to their respective node on the R2R circuit. To test the range of the 

## Loading Effects
Obviously you are going to be making this type of circuitry to drive something. This introduces the idea of loading effect, wherein your circuit will perform differently based on what is going to be attached to it. For each of these implementations, try placing a variety of resistors from 100 ohms up to see what happens to your output signal and comment on what is happening.

## Deliverables
Along with what was asked in each of the parts above, for each implementation, you need to generate at least one triangle wave from your microntroller. This can be done by simply incrementing and decrementing values that are being sent to your circuit. You need to measure the output of each one of these along with taking the FFT on the scope of each one. The span on the FFT will need to go from 1kHz to about 50kHz if possible. You then need to compare the integrity of each signal by analyzing the difference in frequency components.

The README for this part is going to be mainly about the results of your measurement along with information on the implementation. You need to also talk about how you generated the triangle wave, but do not give me a dissertation on it. Since this is going to be talking about hardware, you need to place in the README a Bill Of Materials listing all hardware used as well as link to a Digikey cart which contains the parts needed in the right quantity. You do not need to include things like your F5529 or the breadboard or wires.