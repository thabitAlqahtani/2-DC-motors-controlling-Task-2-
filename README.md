intorduction:
This task is about designing and programming a circuit that controls 2 DC motors to move clockwise and counter-clockwise. These DC motors are used to move the tyres that move the base of the robotic arm. That is done by connecting these DC motors to H bridge drive that controls the motors, and connect it to Arduino. I added the idea of placing a switch, so that if the switch not On the motors will go clockwise, and if it is ON it will go counter-clockwise.

The circuit:
In the attached photo (named Task2-DCmotor circuit) there is the circuit that is used in this task, it is explained in the following steps:
  1- Connect the positive and ground ports of the Battery to the positive and negative nods respectively in the breadboard, and connect the ground port of the arduino to the         ground of the breadboard.
  2- using the H bridge drive (i used L293D because it is available in tinckercad), connect port 1 and port 9 of the drive to one of the digital ports of Arduino, these ports is     used to decide the speed of the motor.
  3- connect port 2 and port 7 and port 10 and port 15 of the drive to one of the digital ports of Arduino, these ports decide in which direction every motor will go, for motor     one for example, if port 2 (IN1) is low, and port 7 (IN2) is high it will go clockwise, and if port 2 high and port 7 low, it will go counter clockwise, and the same for the       other motor.
  4- connect port 2 and port 7 to the first motor, port 2 to the positive and port7 to the negative. connect port 11 and port 14 to the second motor. these ports are the outputs     to the motor that move it.
  5- connect ports 8 (VCC1) and 16 (VCC2) of the drive to the positive node, and connect ports 4,5,12 and 13 of the drive to the ground.
  6- place a switch and connect the positive and negative sides of it to the ones of the circuit, and connect the middle one to one of the digital ports of Arduino.
  
The code:
in order to control the circuit, i used the code (named Task2-DCmotor), firstly, i started by defining SW which is the switch, then, in the setup, i defined every pin as output, excipt the one of the switch because it is input. after that, inside the loop i defined the switch to read the values comming from port 7. then, if the switch is ON, it will go forward, if off, it will go backward, so, inside if function i put the statment "not equal to zero", in this case using degetalWrite i made IN1 low and IN2 High and IN3 low and IN4 High, in else function i reverse high to low and low to high so that it goes other direction. i used analogWrite for EN1 and EN2 so that it controls the speed of the motors.
