# Hbrage-with-DCmotor

The project aims to control a DC motor using an Arduino Uno board and a push button. The button acts as a switch to turn the motor on and off.

### Circuit:


![image alt](https://github.com/safaais/Hbrage-with-DCmotor/blob/e031ede86e6642a57432f4cc51d23d64137e1192/IMG_2712.jpg)

https://www.tinkercad.com/things/9z01HFvxAjG-brilliant-migelo


### Code:

```
int speed1=0,speed2=0,x=0, pwm=0;
void setup()
{
 pinMode(3,OUTPUT);
  pinMode(6,OUTPUT);
  pinMode(7,OUTPUT);
pinMode(4,INPUT);
digitalWrite(4,HIGH);
pinMode(5,INPUT);
digitalWrite(5,HIGH);
}

void loop()
{
  
  
  speed1=digitalRead(4);
speed2=digitalRead(5);

if(speed1==LOW)
{x=3;
	digitalWrite(6,HIGH);
 	digitalWrite(7,LOW);
}
if(speed2==LOW)
{x=5;
	digitalWrite(7,HIGH);
 	digitalWrite(6,LOW);
}
  
  
  
pwm=map(x,0,5,0,255);
analogWrite(3,pwm);
  
  
}
```
