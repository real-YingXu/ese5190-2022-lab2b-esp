### TODO:

Create a REPL to let you read and write RP2040 registers from a console. You should be able to:
- select any 32-bit address to read/write (even if not a valid RP2020 address)
- read/write any 32-bit value to this address
- read/write using any of the atomic bit-setting aliases and a 32-bit mask

#Introduction:
In this part, we will basically use RP2040. The ideal program should be that when the program starts, it will ask the user to select/input a register address then choose to read/write. Once it finished expected reading/writing, it will print a success message from the console.


#code


#include <stdio.h>
#include <stdlib.h>
#include "pico/stdlib.h"
#include "ws2812.h"

#include "pico/stdlib.h"
#include "hardware/pio.h"
#include "hardware/clocks.h"
#include "ws2812.pio.h"
#include "registers.h"

#define IS_RGBW true
#define NUM_PIXELS 150

#ifdef PICO_DEFAULT_WS2812_PIN
#define WS2812_PIN PICO_DEFAULT_WS2812_PIN
#else

// default to pin 2 if the board doesn't have a default WS2812 pin defined

#define WS2812_PIN 12
#define WS2812_POWER_PIN 11
#endif



int main() {
    stdio_init_all();

    PIO pio = pio0;
    int sm = 0;
    uint offset = pio_add_program(pio, &ws2812_program);
    turn_on_power();
    ws2812_program_init(pio, sm, offset, WS2812_PIN, 800000, IS_RGBW);


    uint32_t input_address = 0x00000000;
    ADDRESS address = 0x00000000;
    VALUE value;
    int mode;

    while (true) {
        printf("Start. \n");

        // address selection
        printf("Enter an address you want to read/write: \n");
        scanf("%x", &input_address);  
        printf("Address is %x\n",input_address);
        address = (ADDRESS) input_address;

        // mode selection
        printf("Enter a mode you want to operate (0 for read/1 for write): \n");
        scanf("%d", &mode);
        
        // reading mode
        if(mode == 0) {
            printf("The data read is: %x\n", register_read(address));
        }
        // writing mode
        else {
            // value input
            printf("Enter an value you want to write in: \n");
            scanf("%x", &value);  
            printf("Value is %x \n",value);
            register_write(address, value);
            printf("The value written in: %x\n", register_read(address));
        }
        sleep_ms(250);

    }

    return 0;

}
