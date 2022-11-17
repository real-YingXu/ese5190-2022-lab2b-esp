### TODO:

- use your Lab 1 firefly code to generate ADPS9960 I2C traffic and display it on a lab oscilloscope
- take a screenshot of some portion of this exchange, and figure out/annotate what's happening based on the protocol documentation in the ADPS9960 datasheet 

### part5

### Introduction

In this part, we will use brightness sensor on APDS9960 connected with RP2040 via I2C and lab1 firefly code to measure SCL and SDK value through oscilloscope. The scope trace will show the I2C bus between RP2040 and APDS9960.

![2e5762c9d4801c056d7840178223c31](https://user-images.githubusercontent.com/114200453/202347142-775cb4ea-bf16-4d05-8fd9-39e6acbc1f6d.jpg)






##
connecting circuit


![image](https://github.com/real-YingXu/lab2bpart/blob/main/ezgif.com-gif-maker%20(4).gif)


##


The yellow channel is clock 


the green channel is data

![image](https://user-images.githubusercontent.com/114256663/200049272-88e6d64f-d10f-4fe2-ab09-5ac8af2a18af.png)


zoom in


![image](https://user-images.githubusercontent.com/114256663/200049369-892c9b4b-5795-4f56-91e8-bebc62b50822.png)

##

In the low light:
![image](https://user-images.githubusercontent.com/114256663/200020409-17cd1d22-9768-4415-bcbd-79aded153323.png)



##
In the high light:
![image](https://user-images.githubusercontent.com/114256663/200020473-a3027871-029e-4084-b4fc-a3a4cbc0cdab.png)


##

 code

![image](https://user-images.githubusercontent.com/114256663/200028001-01f1c5c0-1d48-40ad-8026-5ea29265c68c.png)






