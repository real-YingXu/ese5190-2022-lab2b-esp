### TODO:

Create a REPL to let you read and write RP2040 registers from a console. You should be able to:
- select any 32-bit address to read/write (even if not a valid RP2020 address)
- read/write any 32-bit value to this address
- read/write using any of the atomic bit-setting aliases and a 32-bit mask

#Introduction:
In this part, we will basically use RP2040. The ideal program should be that when the program starts, it will ask the user to select/input a register address then choose to read/write. Once it finished expected reading/writing, it will print a success message from the console.


###code

![image](https://user-images.githubusercontent.com/114256663/202346026-13f2d1be-616c-4d09-89d8-86324f126968.png)
![image](https://user-images.githubusercontent.com/114256663/202346055-72951495-e101-4401-ac47-314f45e4d027.png)

###result

Firstly we choose the address 0xd0000060, which can be read and edit with 0-31 bits. We first read the original value at the address (0x7fffff) and then modified it as 0x8fffff. The console shows that the value has been successfully edited.


<img width="812" alt="c0aa2e0613abe06ee8e52c8e7b7e364" src="https://user-images.githubusercontent.com/114200453/200707462-23939d56-df64-4e53-aca9-e10345946937.png">

Then we access the address 0xd0000004, the boot button. When we release the button, the read value is 0x200800 and the return value changed to 0x800 when we pressed the button.

![cd50704cb7af7efced7b3f73cd7a0e0](https://user-images.githubusercontent.com/114200453/200717032-e4f219ca-ec10-4f5c-82f4-684a87ea1b0d.png)



