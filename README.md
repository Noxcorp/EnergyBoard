## Description
	The EnergyBoard is an energy measurement processor for polyphase power-monitoring 
	systems. It is designed for real-time monitoring for a variety of typical three-phase 
	configurations in industrial applications. The MAX78630 provides up to six analog 
	inputs for interfacing to voltage and current sensors. Scaled voltages from the 
	sensors are fed to the single converter front-end using a high-resolution delta-sigma 
	converter. Supported current sensors include current transformers (CTs), Rogowski 
	coils, and resistive shunts.  
	
	In this Arduino Library we can read all data of energy parameters.

![EB_Block](https://github.com/x2bus/EnergyBoard/blob/master/extras/EnergyBoard_Blok.jpg?raw=true)

## Functions

* float RMS_Voltage(char phase);
* float RMS_Voltage_AVR();
* float INST_Voltage(char phase);
* float FUN_Voltage(char phase);
* float HARM_Voltage(char phase);
* float RMS_Voltage_MIN();
* float RMS_Voltage_MAX();
* float RMS_Current(char phase);
* float RMS_Current_AVR();
* float PEAK_Current(char phase);
* float INST_Current(char phase);
* float FUN_Current(char phase);
* float HARM_Current(char phase);
* float RMS_Current_MAX();
* float ActivePower(char phase);
* float ActivePower_AVR();
* float ReActivePower(char phase);
* float ReActivePower_AVR();
* float ApparentPower(char phase);
* float ApparentPower_AVR();
* float FundamentalPower(char phase);
* float HarmonicPower(char phase);
* float FundamentalVA(char phase);
* float PowerFactor(char phase);
* float PowerFactor_AVR();
* float Frequency(void);
* float Temperature(void);

## Example

	RMS Voltage : 230.51 V
	RMS Voltage Avarage : 71.68 V
	Instantaneous Voltage : 311.41 V
	Fundamental Voltage : 230.51 V
	Harmonic Voltage : 0.00 V
	RMS Voltage MIN Limit : 0.00 V
	RMS Voltage MAX Limit : 660.81 V
	RMS Current : 0.40 A
	RMS Current Avarege: 0.14 A
	PEAK Current : 1.27 A
	Instantaneous Current : 99.57 A
	Fundamental Current : -0.14 A
	Harmonic Current : -0.08 A
	RMS Current MAX Limit : 49.61 A
	Active Power : 55.97 W
	Active Power Avarage : 18.65 W
	ReActive Power : 11.59 VAR
	ReActive Power Avarage : 3.78 VAR
	Apparent Power : 92.73 VA
	Apparent Power Avarage : 30.90 VA
	Fundamental Power : 56.63 W
	Harmonic Power : 0.67 W
	Fundamental Volt Amper : 57.80 VA
	Power Factor : 0.59 
	Power Factor Avarage : 0.59 
	Frequency : 49.00 Hz
	IC Temperature : 18.12 C

## Licences

All source code is licensed under the [MIT License](http://opensource.org/licenses/MIT)

	Copyright (c) 2015 X2bus <info@x2bus.com>
	 
	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is furnished
	to do so, subject to the following conditions:
	 
	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.
	 
	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
	THE SOFTWARE.

## Version History

**1.1.0**
* Error variables added, -1001: Without Data, -1002: Negative Acknowledge, -1003: Command not implemented, -1004: Checksum failed
* Voltage function deployment.
* Voltage function name changed to RMS_Voltage
* New voltage function added INST_Voltage (Per Phase)
* New voltage function added RMS_Voltage_AVR
* New voltage function added FUN_Voltage (Per Phase)
* New voltage function added HARM_Voltage (Per Phase)
* New function added RMS_Voltage_MIN
* New function added RMS_Voltage_MAX
* Current function deployment.
* Current function name changed to RMS_Current (Per Phase)
* New Current function added RMS_Current_AVR
* New Current function added PEAK_Current (Per Phase)
* New Current function added INST_Current (Per Phase)
* New Current function added FUN_Current (Per Phase)
* New Current function added HARM_Current (Per Phase)
* New Current function added RMS_Current_MAX
* ActivePower function deployment. (Per Phase)
* New Current function added ActivePower_AVR
* ReActivePower function deployment. (Per Phase)
* New Current function added ReActivePower_AVR
* ApparentPower function deployment. (Per Phase)
* New Current function added ApparentPower_AVR
* New Current function added FundamentalPower (Per Phase)
* New Current function added HarmonicPower (Per Phase)
* New Current function added FundamentalVA (Per Phase)
* PowerFactor function deployment. (Per Phase)
* New Current function added PowerFactor_AVR
* Frequency function deployment.
* Temperature function deployment.
  
**1.0.2**  
* IC Startup commands converted to HEX format.
* Voltage commands converted to HEX format.
* CommandSend function commands converted to HEX format.
* 'print' functions converted to 'write'
* Checksum equation converted to HEX
