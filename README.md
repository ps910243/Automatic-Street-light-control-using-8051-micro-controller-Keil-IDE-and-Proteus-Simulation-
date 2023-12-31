# Automatic-Street-light-control-using-8051-micro-controller-Keil-IDE-and-Proteus-Simulation-
The objective of an automatic street light system using the 8051 microcontroller is  to design and implement a smart lighting solution for streets and public areas that  can automatically control the street lights based on environmental conditions and  time of day.
Abstract:
Hardware / Software Requirements:
   The objective of an automatic street light system using the 8051 microcontroller is
 to design and implement a smart lighting solution for streets and public areas that
 can automatically control the street lights based on environmental conditions and
 time of day.
 The "Automatic Street Light Control System Using 8051 Microcontroller" is a smart
 lighting solution designed to efficiently manage street lighting by incorporating a
 microcontroller-based control system. This system enhances energy conservation
 and ensures the safety and convenience of pedestrians and motorists.
 ● 8051 microcontroller (e.g., AT89S52)
● Light-dependent resistor (LDR)
● Relay module
● LED street lights or a simulation circuit
● Power supply
● Resistors, capacitors, and connecting wires
Working Principle:
Approach / Methodology / Programs:
 The "Automatic Street Light Control System Using 8051 Microcontroller" is a smart
 lighting solution designed to efficiently manage street lighting by incorporating a
 microcontroller-based control system. This system enhances energy conservation
 and ensures the safety and convenience of pedestrians and motorists.

  1.Connect the LDR in a voltage divider configuration with a fixed resistor. This will create a voltage that varies with ambient light conditions.
2.Connect the analog output of the voltage divider to one of the analog pins of the 8051 microcontroller. This will allow the microcontroller to read the analog value from the LDR.
3.Connect the relay module to one of the digital output pins of the 8051 microcontroller. The relay module should control the power supply to the LED street lights. Ensure proper connections to the relay, including a flyback diode.
 Flowchart:
4.Connect the LED street lights to the normally open (NO) or common (COM) terminal of the relay so that they can be switched on or off by the relay.



Code: #include<reg51.h> sbit sensor1=P1^0; sbit sensor2=P1^1; sbit sensor3=P1^2; //sensor on street// sbit load1=P2^0; sbit load2=P2^1; sbit load3=P2^2;

 //street light connections//
void main()
{
load1=load2=load3=0; sensor1=sensor2=sensor3=0;//optinal logic based while(1)
{
if(sensor2==1)
{
load1=1;//street light 1 on load2=0;//street light 2 off load3=0;//street light 3 off
}
if(sensor2==1)
{
load1=0;
load2=1;//street light 2 on
load3=0; }
if(sensor3=1) {
load1=0;
load2=0;
load3=1;//street light 3 on
}

 } }
