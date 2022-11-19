# 

University of Pennsylvania, ESE 5190: Intro to Embedded Systems, Lab 2B

Ying Xu
    anniexu6@seas.upenn.edu
Tested on: 
mac OS bigsur
version 11.6
macbook air（M1 2020)



##



1）Gif：

![image](https://github.com/real-YingXu/Ying-Xu_lab2b_proposal/blob/main/ezgif.com-gif-maker%20(6).gif)


code：
![image](https://user-images.githubusercontent.com/114256663/197107037-5d008000-a458-4df6-b1a3-4a5c94a75007.png)





##


2)Outline：

We plan to build a series of leds that is connected in parallel.

we will then make the a light alerting clock that is designed for traffic lights. 

The red light will first flash with showing :"Wait", 

then the yellow light flash many times and stop.

Finally, the blue light will flash with showing "Ready".


I think it‘s cool because there are several GPIO pins on QT-PY2040 which can drive different color LEDs to connect in parallel. and the circuit is like the traffic lights that  flash  in sequence.


##


3)Components：

macbook air（M1 2020）

QT-PY 2040 and sensor APDS9960

Breadboard

Different Resistors (330ohm - 1k ohm) 

Different color LEDs


##


4）Question：

What’s value return to RP2040 when the sensor detects the brightness？

How many leds can be used mostly？

For the protective resistor selection, why should we only use the 330ohms and 1k ohms resistor instead of other values?


##

Update November3







##
soldering processing


![image](https://github.com/real-YingXu/Ying-Xu_lab2b_proposal/blob/main/ezgif.com-gif-maker%20(4).gif)





##

assemble circuit


![image](https://user-images.githubusercontent.com/114256663/199850350-a38d79eb-39a6-42e4-9e3c-800653c8b56a.png)





![image](https://user-images.githubusercontent.com/114256663/199846927-e245cfc3-8366-462d-81d2-17a166f8abf4.png)






##

Demo gif

![image](https://github.com/real-YingXu/Ying-Xu_lab2b_proposal/blob/main/led.gif)


##

code
![image](https://user-images.githubusercontent.com/114256663/199849162-e87412ba-b788-4742-8233-47a635fa1133.png)

![image](https://user-images.githubusercontent.com/114256663/199849179-6b090980-e324-4314-b058-4d0a891601d8.png)

![image](https://user-images.githubusercontent.com/114256663/199849200-ac34e60f-8bc9-4bb9-86d5-147acf832745.png)































