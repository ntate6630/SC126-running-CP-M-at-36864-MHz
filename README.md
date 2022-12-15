# SC126-running-CPM-at-36864-MHz
Code to change register settings to double CPU clock speed and alter WAIT states and UART0 and UART1 config.

Assembled with the Z180 assembler and linker from the Hightech C toolchain for CP/M.
Please install HiTechC 3.09 to your Steve Cousins Z180 system running CP/M. Download here: http://www.z80.eu/c-compiler.html

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

UPDATE:

Added a selection of settings for changing the number of WAIT STATE's within the code. Uncomment the line thats most suitable for your setup.

The options are:

ORIGINAL SETTING - The default setting as tried and tested on my own hardware. This should work with the majourity of basic Steve Cousins Z180 setups.

LONGEST WAIT TIMES FOR SLOW MEMORY AND SLOW I/O - Try this setting if you experience errors or instability when running the system in the FAST mode.

ORIGINAL MEMORY SPEED - SLOW I/O - If your Z180 system is running CP/M correctly but you are experiencing errors with slow I/O devices 
connected to your setup then use this setting to give more WAIT STATE's to external I/O devices. 

Please see the section in the "FAST.ASM" source file titled - "; ******	SETUP WAIT STATES	******" 
for setting details. Only uncomment one of the lines in the source code for wait settings.


#NEW SLOW UTILITY

This returns the CPU back to 18.432 MHz and WAIT states and UART settings back to the way it is after boot up without the need to do a reboot.

Assembled with the Z180 assembler and linker from the Hightech C toolchain for CP/M
Please install HiTechC 3.09 to your Steve Cousins Z180 system running CP/M. Download here: http://www.z80.eu/c-compiler.html

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




