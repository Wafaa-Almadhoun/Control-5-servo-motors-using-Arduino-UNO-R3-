
# Control-5-servo-motors-using-Arduino-UNO-R3-

## Table of contents
* [Introduction](#Introduction)
* [Technologies](#technologies)
* [Components required](#Components-required)
* [Connections](#Connections)
* [Block diagram & simulation ](#Block-diagram-&-simulation)



## Introduction
This project is to control 5 servo motors using Arduino UNO R3 simulated with TINKERCAD circuit , The servo motor is used in robotics to activate movements, giving the arm to its precise angle , so we used it with several projects like robot arm , spider robot and  robotic vehicle ,We will cover several topics : 👍 
 1. servo motor rotate 90 degrees .
 2. servo motor rotate 90 degrees and back to 0 degree after 3 sec .
 3. Control multiple servo motors using Potentiometers .

## Technologies
Project is created with:
* Arduino IDE 1.18.15 [To Downloud](https://www.arduino.cc/en/software)
* AUTODESK TINKERCAD [Open](https://www.tinkercad.com/)
	
## Components required
1. Arduino ANO
2. 5 servo motors MG995
3. jumper wirs
4. 5 potontial meters 10 K ohm 
5. bettrey  5 volt
6.breadboard

## Connections
Connection pins:

5V:  Power (red)

Gnd: Ground (black)

13,10,7,5,3 : Digital Signals (orange, yellow, green, blue, purple)

A0,A1,A2,A3,A4 : Analog Signals (violet, brown, grey, cyan,pink)

## Block diagram & simulation
### 1-servo motor rotate 90 degrees . [see here](https://www.tinkercad.com/things/gbEAiV1jBww-task-12-/editel?sharecode=BJKBPih72RmLoE9rHIyFUbfSYzqZ60Z83fKnogQJ0Lg)

![1](https://user-images.githubusercontent.com/64277741/122782880-c02eb000-d2b9-11eb-8eb7-d6fee3be6355.PNG)
Figure (1): Servo Motor at initial value (0 degree

After 1 sec
![1 2](https://user-images.githubusercontent.com/64277741/122783332-24ea0a80-d2ba-11eb-81ef-cee1f5e9950c.PNG)
Figure (2): Servo Motor at 90 degrees 

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
![1](https://user-images.githubusercontent.com/64277741/122786121-a5116f80-d2bc-11eb-9a95-e5d2b8a3b9ab.PNG)
Figure (3): Servo Motor at initial value (0 degree)

After 3 sec 
![1 2](https://user-images.githubusercontent.com/64277741/122786155-ae9ad780-d2bc-11eb-8f7c-c81f11a682b0.PNG)
Figure (4): Servo Motor at 90 degrees
After 6 sec back to 0 
![1](https://user-images.githubusercontent.com/64277741/122786121-a5116f80-d2bc-11eb-9a95-e5d2b8a3b9ab.PNG)
Figure (5): Servo Motor back from 90 to 0 degree

#### The code 
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
delay(3000); 
  
Servo1.write(90); 
   
Servo2.write(90); 
    
Servo3.write(90); 
   

Servo4.write(90); 


Servo5.write(90); 
  
delay(3000);
  
Servo1.write(0);
Servo2.write(0);
Servo3.write(0);
Servo4.write(0);
Servo5.write(0);




}
`_


### 3- Control multiple servo motors using Potentiometer [see here](https://www.tinkercad.com/things/jBKW8pofJhZ-task-3-control-servo-motor-using-potentiometer/editel?sharecode=FqY5TjQ9On_IY1DgVje0gg_ci8Gl3PQnv6i9iKbzVOA)
At begin
![3](https://user-images.githubusercontent.com/64277741/122786908-75169c00-d2bd-11eb-9624-60cee51a1ea6.PNG)
Figure (6): Five Servo Motor with Five Potentiometers

After start simulation ![4](https://user-images.githubusercontent.com/64277741/122787141-b3ac5680-d2bd-11eb-97f9-08a8c668f9b1.PNG)
Figure (7): Changing the angles of Servo Motors according to change the angles of Potentiometers

#### The Code 
`#include <Servo.h>

Servo s;

Servo t;

Servo u;

Servo v;

Servo w;



int potpin = 0;
int potpin2 = 1;
int potpin3 = 2;
int potpin4 = 3;
int potpin5 = 4;

int val = 0;
int val2 = 0;
int val3 = 0;
int val4 = 0;
int val5 = 0;


void setup()
{

  s.attach(13);  // attaches the servo on pin 13 to the servo object
  t.attach(10);
  u.attach(7);
  v.attach(5);
  w.attach(3);
}

void loop()
{

val = analogRead(potpin);
val = map(val, 3, 1023, 0, 176);

s.write(val);

delay(25);

val2 = analogRead(potpin2);
val2 = map(val2, 0, 1023, 0, 180);

t.write(val2);

delay(25);

val3 = analogRead(potpin3);
val3 = map(val3, 0, 1023, 0, 180);

u.write(val3);

delay(25);

val4 = analogRead(potpin4);
val4 = map(val4, 0, 1023, 0, 180);

v.write(val4);

delay(25);

val5 = analogRead(potpin5);
val5 = map(val5, 0, 1023, 0, 180);

w.write(val5);

delay(25);

}
`_




