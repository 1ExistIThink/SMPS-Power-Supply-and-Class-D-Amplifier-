### Sources:
 

### Speaker Drivers:
## Tweeter:
https://www.parts-express.com/Dayton-Audio-RST28F-4-1-1-8-Reference-Series-Fabric-Dome-Tweeter-4-Ohm-275-141?quantity=1
* Power Handling (RMS)	`80 W`

## Woofer:
https://www.parts-express.com/Dayton-Audio-RS150-8-6-Reference-Woofer-295-354?quantity=1
* Power Handling (RMS)	`40 W`

### Calculations and Selections:
PWR: 40 + 80 = 120 `Wrms`
PWR output: Class D efficiency (80% worst case) = 120/0.9 * 1.5 = `200 W`

Connect `120 V` outlet to SMPS, output `24 V` to Class D amplifier

Switching Frequency: `250kHz`
* 250kHz/20kHz = 12.5 x higher than audio band, will likely not be heard
* Smaller component sized
* Increased switching losses than lower frequencies

Current Output: P = IV -> I = P/V = 200W / 24Vdc = `8.33 A`

Vdc (after rectification) = 120*sqrt(2) = `169.7 Vpeak`

Efficiency: `85 %`
* Relatively decent efficiency, very achievable

Specifications
* Input Voltage: `120 Vrms`
* Rectified Input Voltage: `169.7 Vpeak`
* Output Power: `200 W`
* Output Voltage: `24 Vdc`
* Output Current: `8.33 A`
* Switching Frequency: `250 kHz`
