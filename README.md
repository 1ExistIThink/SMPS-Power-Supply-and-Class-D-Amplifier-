Project:
Design a Class D bookshelf speaker with STM32 DSP

### Calculations
Crystal Calculations: 
```
From Datasheet: 
- 18pF load capacitance 

Ceq = (1/C1 + 1/C2)^(-1) + Cstray
Since C1 = C2 = C:
Ceq = C/2 + Cstray

Solve for C (5pF estimate):
C/2 = Ceq - Cstray
C = 2(Ceq - Cstray)
C = 2(18pF - 5pF)
C = 26pF
```
We will choose 25pF, which is available on digikey and is close to our value. It will be NP0 since we do not want the capacitance to vary with voltage/temperature. 

Using (USBC): 
https://www.digikey.com/en/products/detail/abracon-llc/ABMM2-8-000MHZ-E2-T/1236945

<img width="775" height="377" alt="image" src="https://github.com/user-attachments/assets/fb71a657-7602-422c-87b9-28ab5c26fca8" />

USBC Receptacle: 

5.1k Resistors to ground for detecting a connection. 

Using:
https://www.digikey.com/en/products/detail/molex/2171790001/13913749

Using (TVS Diode IC):
https://www.digikey.com/en/products/detail/stmicroelectronics/USBLC6-2SC6/1040559


Flash:

Using:
https://www.digikey.com/en/products/detail/macronix/MX25L3233FM2I-08G/7402341
Features:
* External 4MB Flash 
* Power 3.3V

SO/SIO1 (PB4) is the flash output, so it goes to MCU MISO.
SI/SIO0 (PB5) the flash input, so it goes to MCU MOSI.
SCLK (PB3) 
