### Sources:
* https://www.electricity-magnetism.org/forward-converter-formula/
* https://www.plexim.com/sites/default/files/tutorials/forward_converter.pdf


Goal: Design a SMPS for bookshelf speakers. Connect `120 V (RMS)` outlet to SMPS, output `24V` to Class D amplifier.
## Topology:
* Forward converter: 
* simple: one MOSFET, cheap, works well
* Transformer Turns Ratio (with half wave the turns ratio is higher) 

### Speaker Drivers:
## Tweeter:
https://www.parts-express.com/Dayton-Audio-RST28F-4-1-1-8-Reference-Series-Fabric-Dome-Tweeter-4-Ohm-275-141?quantity=1

Power Handling (RMS)	`80 W (RMS)`

## Woofer:
https://www.parts-express.com/Dayton-Audio-RS150-8-6-Reference-Woofer-295-354?quantity=1
Power Handling (RMS)	`40 W (RMS)`

### Calculations and Selections:
Power Output: 
* Pspeaker(RMS) + Ptweeter(RMS) = 40 + 80 = `120 W (RMS)`

Desired PWR output:
* Class D efficiency (90%) = 120/0.9 * 1.5 = `200 W (RMS)`

Switching Frequency: `250kHz`
* 250kHz/20kHz = 12.5 x higher than audio band, will likely not be heard
* Smaller component sizing
* Increased switching losses than lower frequencies
* Harder to do layout than lower frequencies 

Output Current: P = IV -> I = P/V = 200W / 24Vdc = `8.33A`

Vdc (after rectification) = 120*sqrt(2) = `169.7Vpeak`

Efficiency: `85%`

Specifications (Summary) 
* Input Voltage: `120 V (RMS)`
* Rectified Input Voltage: `169.7 V (PEAK)`
* Output Power: `200 W (RMS)`
* Output Voltage: `24 V (DC)`
* Output Current: `8.33 A`
* Switching Frequency: `250 kHz`
* Target Efficiency `85 %` 

### Calculations 
Remember we are using a Forward Converter topology 

Rectified Voltage (from NMOS):
* Vp = 120*sqrt(2) = 169.7 V (DC) 
Subtract 1V from Rectification Loss: 
* Vp = 168.7 V (DC)
Add 0.5V for rectification loss:
* Vs = 24.5V
Choosing duty cycle D = 0.45 
* Vs = Vp * D * (Ns/Np) -> Ns/Np = Vs/(Vp * D) = 24.5 / (168.7 * 0.45) = 0.323 turns ratio 















