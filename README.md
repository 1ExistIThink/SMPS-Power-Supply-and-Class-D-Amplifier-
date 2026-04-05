### Sources:
 

### Speaker Drivers:
## Tweeter:
https://www.parts-express.com/Dayton-Audio-RST28F-4-1-1-8-Reference-Series-Fabric-Dome-Tweeter-4-Ohm-275-141?quantity=1

Power Handling (RMS)	`80 Watts`

## Woofer:
https://www.parts-express.com/Dayton-Audio-RS150-8-6-Reference-Woofer-295-354?quantity=1
Power Handling (RMS)	`40 Watts`

### Calculations and Selections:
PWR: `40 + 80 = 120 Wrms`
PWR output: `Class D efficiency (80% worst case) = 120/0.9 * 1.5 = 200W`

Connect `120V` outlet to SMPS, output `24V` to Class D amplifier

Switching Frequency: `250kHz`
	• `250kHz/20kHz = 12.5 x higher than audio band`, will likely not be heard
	• Smaller component sized
	• Increased switching losses than lower frequencies

`P = IV -> I = P/V = 200W / 24Vdc = 8.33A`

`Vdc (after rectification) = 120*sqrt(2) = 169.7Vpeak`

Efficiency: `85%`
	• Relatively decent efficiency, very achievable

SMPS Topologies:
	• Buck Converter
		○  (bad with high voltage no isolation)
	• Flyback Converter
		○ Lower cost
		○ Full Isolation
		○ Simpler math
		○ Usually lower wattage (`<150W`)
Specifications
	• Input Voltage: `120 Vrms`
	• Rectified Input Voltage: `169.7 Vpeak`
	• Output Power: `200 W`
	• Output Voltage: `24 Vdc`
	• Output Current: `8.33 A`
	• Switching Frequency: `250 kHz`
