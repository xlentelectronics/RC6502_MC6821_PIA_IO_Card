# RC6502 MC6821 PIA IO Card

To have IO possibilities with the RC6502, a IO Card with the MC6821 has been developed. To connect the card to the RC6502, just place it in the Backplane. Via jumper J4 you can place the card in the address range you prefer. The included software examples use the base address $C000.
The hardware and software are open licensed.

![Build MC6821 PIA IO Card](\RC6502_MC6821_PIA_Schematic\MC6821_PIA_IO_Card.jpg) 

# Software Examples
In the Software Example folder are some examples how to use the MC6821 PIA IO Card. The examples are created for Krusader v1.3 and for MBASIC.

## Krusader assembler Example
In the Krusader Assembler folder the example MC6821_PingPong_Light_Speedmeter_Color.asm can be found.  This is a fully compatible Krusader v1.3 program. The program lets 8 LEDS running in a pingpong way. The speed can be controlled via the + and - of the numeric keypad of the keyboard.

The following hardware connection has to be made to PORTA and PORTB.
PORTA is connected to 8 LEDS. The Anode of the LEDS are connected with a resistor of 1K between Vcc and corresponding pins PA0 to PA7.
the .asm file can directly be loaded into Krusader v1.3. Make sure before loading the .asm file you have opend Krusader in Editting mode, 000. If you use TeraTerm, you load the .asm via _Send file ..._After successful load, assembler the file and run it via R $0300 (I assume you know how Krusader v1.3 works)

There is also as example the MC6821_PingPong_Light_Speedmeter_Color.woz. This file is the WoZ monmitor compatible file. You can load the .woz file from the Woz Monitor in the same way by using _Send file ..._  

![PINGPONG Running Light](\Software Example\Krusader Assembler\MC6821_PIA_PINGPONG_Speedmeter_Color_0.jpg) 
![Speedmeter Green](\Software Example\Krusader Assembler\MC6821_PIA_PINGPONG_Speedmeter_Color_1.jpg) 
![Speedmeter Yellow](\Software Example\Krusader Assembler\MC6821_PIA_PINGPONG_Speedmeter_Color_2.jpg) 
![Speedmeter Red](\Software Example\Krusader Assembler\MC6821_PIA_PINGPONG_Speedmeter_Color_3.jpg) 


## MBASIC Examples
In the MBASIC folder there are 2 MBASIC examples, MBasic_MC6821_PIA_IO_RunningLight_PortA.bas and MBasic_MC6821_PIA_IO_RunningLight_Speed.bas.

Both MBASIC examples uses the same LED hardware connections as mentioned for the PINGPONG Running Light.An additional piece of hardware is required for the MBasic_MC6821_PIA_IO_RunningLight_Speed.bas.
Connect a push button via 10K resistor to Vcc and the other lead of the push button to GND. Connect PORTB PB7 to the 10K resistor. When you push the button, PB7 will go low.

Start MBASIC and load the .bas file via _Send file ..._ and type RUN to execute the program.

![MBASIC ](\Software Example\MBASIC\MBASIC_MC6821_RL_Speed.jpg) 
