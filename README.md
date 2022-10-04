# SC126-running-CPM-at-36864-MHz
Code to change register settings to double CPU clock speed and alter WAIT states and UART0 and UART1 config.

Assmbled with the Z180 assembler and linker from the Hightech C toolchain for CP/M

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
