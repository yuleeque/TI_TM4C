


## Setup
note: Detected in Devices as "In-Circuit Debug Interface".
In MDK v5.29 as well as newer versions of MDK the support 
for the Stellaris ICDI debug adapter has been removed.
There is an add-on Stellaris ICDI installer that supports MDK v5.29. 
Download ( https://developer.arm.com/documentation/ka002280/latest )
and put it in C:\Keil_v5\ARM\PACK\.Download, then run.
Or use this EXE saved in /docs.

0. install Stellaris ICDI Debugger for Keil
1. New project -> Select Device for Target 'Target 1' -> TM4C123GH6PM
2. Manage Run-Time Environment -> CMSIS: CORE (v5.5.0) and Device: Startup (v3.2.2)
3. Add Existing Files to Group 'Source Group 1'... (main.c, TODO.h, TODO.c)
4. Options for Target 'Target 1' -> Target -> Code Generation -> ARM Compiler -> Use default compuler version 5
5. Options for Target 'Target 1' -> Debug -> Stellaris ICDI -> Settings -> Configuration -> Debug -> Mode JTAG, Clock 1MHz, Reset SYSRESETREQ, Verify flash content on Debug
6. Options for Target 'Target 1' -> Debug -> Stellaris ICDI -> Settings -> Configuration -> Flash -> Page Erase (erase only necessary pages), Program, Verufy, Reset and Run