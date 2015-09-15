# ciclo-for-en-ensamblador
this is a cicly for
------------------------
LDS R0,0x100; leo A
LDS R1,0x101: leo B
CP R0,R1;     si son iguales, la bandera Z=1 si son diferentes Z=0
BRNE Zescero; Brinca a Zescero
LDI R0,0x00;  carga R0 con una constante 0
STS 0x00,R0;  Guarda en 0x100 R0
INC R1
STS 0x101,R1
JMP continuar
Zescero
NEG R0
STS 0x100,R0
LDI R1,0xFF
STS 0x101,R1
continuar  
