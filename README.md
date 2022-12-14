# SC126-running-CPM-at-36864-MHz
Code to change register settings to double CPU clock speed and alter WAIT states and UART0 and UART1 config.

Assembled with the Z180 assembler and linker from the Hightech C toolchain for CP/M.
Please install HiTech C to your Steve Cousins Z180 system running CP/M. Download here: http://www.z80.eu/downloads/z80v309.lzh

Using other assemblers may require small changes to the code.

Using any text editor in CP/M to write out the code and save the file as:-   FAST.ASM

From the comand line in CP/M to assemble the .ASM 
C:ZAS C:FAST.ASM 

The result is FAST.OBJ

Run the linker
C:LINK -C100H -OFAST.COM C:FAST.OBJ

Creates an executable file
C:FAST.COM

Type FAST to run the utility. 

Youtube video shows demonstration of before and after running the overclock utility. (NOTE this demo video is now old and does not reflect the latest updates.)
https://www.youtube.com/watch?v=JDSr2Kb83AI

DISCLAIMER: This code is experimental and alters settings that overclock the Z180 CPU, changes WAIT timings and changes UART settings and I can not guarantee the system will run reliably on every setup.


#NEW SLOW UTILITY

This returns the CPU back to 18.432 MHz and WAIT states and UART settings back to the way it is after boot up without the need to do a reboot.

Assembled with the Z180 assembler and linker from the Hightech C toolchain for CP/M
Please install HiTech C to your Steve Cousins Z180 system running CP/M. Download here: http://www.z80.eu/downloads/z80v309.lzh

Using other assemblers may require small changes to the code.

Using any text editor in CP/M to write out the code and save the file as:-   SLOW.ASM

From the comand line in CP/M to assemble the .ASM 
C:ZAS C:SLOW.ASM

The result is SLOW.OBJ

Run the linker
C:LINK -C100H -OSLOW.COM C:SLOW.OBJ

Creates an executable file
C:SLOW.COM

Type SLOW to run the utility.




