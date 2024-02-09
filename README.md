# Greenhouse-Automation.-Embedded-STM32
Project Specifications:
The main objective of this project is to build an automated system in a greenhouse capable of making decisions based on the measurements of environmental variables using the STM32 NUCLEO-F446RE MCU and programming it by means of the methods acquired through the course.

Automation of tasks in a greenhouse.
The system is accompanied by compatible sensors and actuators, capable of monitoring the behavior of environmental variables temperature and air humidity. An automated irrigation system capable of making decisions based on these measurements will be designed and implemented.
Temperature control: One common system is using a called zenithal ventilation, which is a kind of moving window installed in the roof that allows escaping hot air from inside. It is activated by means of the geared motor that will move the rack which in turn moves the window. Considering the measurement of a temperature sensor, control needs to be implemented acting on the opening angle of the window (by a servomotor) to meet this desired temperature setpoint.
 
Humidity Control: Ventilation control is  essential  to  generate  the  appropriate humidity inside the greenhouse, for this, there are several methods, one of them is the incorporation of side fans that can extract excess humidity inside the greenhouse.

And last, there is the control of the irrigation system that is governed by the time of day and the kind of plant. The irrigation pump is turned on at a certain moment of the day (10:00 am), carrying the water to the ground through sprinklers until one of these conditions be meet:
o	Overcome certain threshold on soil humidity (measured by a sensor).
o	After a certain period of time
Both conditions depend on the type of crop and are updated when the button (for change it) is pressed.
Inputs: Temperature sensor, Ambient humidity sensor, Crop button selector, Soil humidity sensor (Analog potentiometer)

Outputs: 12V DC motor, Servomotor, Relay (Irrigation Pump), LCD Display.
 
We consider 3 types of crops, Tomato, Lettuce and Cucumber. The parameters are shown below:
Tomato: Temperature: 20  -  30°C. Relative soil humidity: 60– 75% Irrigation time: 2h

Lettuce: Temperature: 15– 18°C.
Relative soil humidity: 60– 80% Irrigation time: 1h.

Cucumber: Temperature: 22 – 26°C. Relative soil humidity: 80%. Irrigation time: 1:20 h.

The system is formed by:
STM32F446RET6 MCU JGA25-371 12V DC Motor
MG90S Servomotor ELEGOO 16x2 LCD Module
AZDelivery LCD I2C Serial Interface DTH11 Temperature/Humidity Sensor L298N Motor Shield.
470 Ω Potentiometer
10K Resistor
EFISH & ALSISK 12V 1A Power Adapter

Environmental variables, temperature and humidity are measured, then the PID algorithms calculate the needed angle output for the damper system to regulate the airflow (temperature regulation) and simultaneously regulate the fan speed (humidity regulation) for extract humidity excess.

The main variables are then shown in a display, which are:
•	Measured Temperature
•	Measured Humidity
•	Irrigation Time
•	Setpoints
