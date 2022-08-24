# purchase link

[Click to buy](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4002-21223910208.11.6e286a4biB4k47&id=671186893005)

# picture display

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/main/Voltage%20to%20PWM/image/Front%20display.jpg" width="400">

# Introduction
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The voltage to PWM module can convert 0-5V voltage into 0%-100% PWM signal output. Users can control the output PWM signal duty cycle by adjusting the voltage of the input port.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The module has a potentiometer interface reserved for users to adjust the duty cycle of the output PWM signal through the potentiometer. Users can purchase it if necessary. The model is WH148 single-connected potentiometer. The module is welded by default with 5.0mm terminals, and an extra 2.54 mm is reserved. The mm pin header interface is used for signal input and output, and the user can solder it by himself (the power supply is limited to the power supply of the 5.0mm terminal block).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This module can cooperate with motor/LED and other PWM-controlled driver boards to quickly realize motor speed regulation/light brightness adjustment and other functions.

# parameter
| Voltage | DC3-6V / DC 9-30V |
|--|--|
| Current | 6-14 mA (no-load test, the actual use may be slightly higher) |
| Input Signal | 0-5V (Above 5.5V may cause permanent damage to the circuit) |
| PWM frequency error | ±3% |
| Duty cycle error | ±1% |
| PWM amplitude | 5V (bulk can be customized by contacting customer service) |

# Pin description
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Users can refer to the picture below or the silk screen on the back of the module

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/main/Voltage%20to%20PWM/image/Bottom%20display.jpg" width="400">

| pin name | pin function |
|--|--|
| 3-6V | 3-6V power supply positive pole, choose one of 9-30V port |
| 9-30V | 9-30V power supply positive, choose one of the 3-6V ports |
| GND | Negative power supply |
| AIN | Voltage signal input terminal |
| PWMA | PWM signal output, the duty cycle increases as the voltage increases |
| PWMB | PWM signal output, the duty cycle decreases as the voltage increases |

# Instructions for use
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Correctly connect the power supply voltage between the 3-6V or 9-30V port and GND, and connect the analog voltage signal that needs to be input to AIN. The signal needs to share the ground with the module, so the negative electrode of the signal also needs to be connected to GND. Change The input analog voltage, the corresponding PWMA and PWMB port output signal duty cycle will also change.

# Reserved interface

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/main/Voltage%20to%20PWM/image/Jumper%20pads.jpg" width="400">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There are four jumper pads PA, PB, LA, and LB reserved on the board.
&nbsp;

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Since the PWMA and PWMB signal output ports of the board are connected in series with 100Ω resistors, it can prevent the signal port from being burned out due to excessive current at the signal output port to a certain extent. Considering the needs of a small number of users, we provide PA or PB jumper pads, short-circuit You can skip the 100Ω resistor and connect it directly to the signal output. PA corresponds to PWMA signal, and PB corresponds to PWMB signal. Generally, users can ignore this section if they don’t have this requirement or don’t understand it.


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There is a blue LED on the module, which is pulled down from the PWMB signal output port. When the voltage of the AIN port rises, the LED brightness decreases. If the LED is not required to light up, you can use a soldering iron to disconnect the LB connection. The default LB jumper is soldered. short circuit.

# Module size
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Length x Width: 35.3 x 29.25 mm (manual measurement will be biased)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The positioning hole is 3.1mm, users can match with 3mm round head screws

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/main/Voltage%20to%20PWM/image/Dimensions.jpg" width="400">

# Precautions
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①The power supply voltage of the 3-6V port of the module should not exceed 8V. It is recommended to use it between 3V and 6V. At the beginning of the module design, there is a certain margin, but do not exceed 8V for power supply.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②The power supply voltage of the 9-30V port of the module should not exceed 35V. It is recommended to use it between 9V and 30V. Also, this port has a certain margin at the beginning of the module design, but do not exceed 35V for power supply.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;③Regarding the duty cycle of the output PWM, since there will be an imbalance problem at the zero point, the duty cycle of the module will directly become 0% when it is lower than about 2%, and it will directly become 100% when it is higher than about 98%.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;④The PWM frequency output by the module has multiple versions of 1K, 10K, 25K, 50K HZ. Users can contact customer service to customize in batches. In addition, the default interface of this version of the potentiometer matches the WH148 single-connection model, and can also contact customer service to customize in batches.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⑤The provided potentiometer interface can use a 10K potentiometer. When using an external potentiometer, please do not connect the AIN signal input terminal to the signal. Otherwise, when the potentiometer is screwed to both ends, there is a high probability that the circuit board will be damaged or even risked. smoke burned.



