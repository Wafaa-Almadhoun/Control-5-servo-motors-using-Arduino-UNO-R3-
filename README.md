
# Control-5-servo-motors-using-Arduino-UNO-R3-

## Table of contents
* [Introduction](#Introduction)
* [Technologies](#technologies)
* [Components required](#Components-required)
* [Block diagram & simulation ](#Block-diagram-&-simulation)


## Introduction
This project is to control 5 servo motors using Arduino UNO R3 simulated with TINKERCAD circuit , The servo motor is used in robotics to activate movements, giving the arm to its precise angle , so we used it with several projects like robot arm , spider robot and  robotic vehicle ,We will cover several topics : 👍 
 1. servo motor rotate 90 degrees .
 2. servo motor rotate 90 degrees and back to 0 degree after 3 sec .
 3. Control multiple servo motors using Potentiometers .

## Technologies
Project is created with:
* Arduino IDE 1.18.15 [To Downloud](https://www.arduino.cc/en/software)
* ATODESK TINKERCAD [Open](https://www.tinkercad.com/)
	
## Components required
1. Arduino ANO
2. 5 servo motors MG995
3. jumper wirs
4. 5 potenciometro 10 K ohm 
5. bettrey  5 volt
6.breadboard

## Block diagram
### 1-servo motor rotate 90 degrees . [see here](https://www.tinkercad.com/things/gbEAiV1jBww-task-12-/editel?sharecode=BJKBPih72RmLoE9rHIyFUbfSYzqZ60Z83fKnogQJ0Lg)

![1](https://user-images.githubusercontent.com/64277741/122782880-c02eb000-d2b9-11eb-8eb7-d6fee3be6355.PNG)
after 1 sec
![1 2](https://user-images.githubusercontent.com/64277741/122783332-24ea0a80-d2ba-11eb-81ef-cee1f5e9950c.PNG)
#### The Code 
`#include <Servo.h> 
 
int servoPin = 3;
int servoPin2 = 5;
int servoPin3 = 7;
int servoPin4= 10;
int servoPin5= 13;


 Servo Servo1, Servo2, Servo3, Servo4, Servo5;
void setup() { 
   // We need to attach the servo to the used pin number 
   Servo1.attach(servoPin); 
Servo2.attach(servoPin2);
Servo3.attach(servoPin3); 
Servo4.attach(servoPin4);
Servo5.attach(servoPin5); 
 
}
void loop(){ 
delay(1000); 
  
Servo1.write(90); 
   
Servo2.write(90); 
    
Servo3.write(90); 
   

Servo4.write(90); 


Servo5.write(90); 
  
delay(1000);
  
Servo1.write(0);
Servo2.write(0);
Servo3.write(0);
Servo4.write(0);
Servo5.write(0);




}
`_

### 2-servo motor rotate 90 degrees and back to 0 degree after 3 sec .[see here ](https://www.tinkercad.com/things/gbPPDKDpC4S-task-12-servo-motor-0-90/editel?sharecode=F5nGzvf_Q4hBc8hK6pDw1buUxTyYmv8P1hEopJZUgGc)


### 3- Control multiple servo motors using Potentiometer [see here](https://www.tinkercad.com/things/jBKW8pofJhZ-task-3-control-servo-motor-using-potentiometer/editel?sharecode=FqY5TjQ9On_IY1DgVje0gg_ci8Gl3PQnv6i9iKbzVOA)
