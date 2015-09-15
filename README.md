# ciclo-for-en-ensamblador
this is a cicly for
------------------------
LDS R0,0x100;  leo A
LDS R1,0x101:  leo B
CP R0,R1;      si son iguales, la bandera Z=1 si son diferentes Z=0
BRNE Zescero;  Brinca a Zescero
LDI R0,0x00;   carga R0 con una constante 0
STS 0x00,R0;   Guarda en 0x100 R0
INC R1;        incrementa el registro R1 
STS 0x101,R1;  guarda R1 en la localidad de memoria
JMP continuar; brinca a la etiqueta continuar
Zescero;       etiqueta "Zescero"
NEG R0;        niega el registro R0, complemento a dos
STS 0x100,R0;  guarda R0 en la localidad de memoria
LDI R1,0xFF;   carga inmediatamente la constante en el registro R1
STS 0x101,R1;  Guarda el registro R1 en la localidad de memoria
continuar      etiqueta "continuar"
