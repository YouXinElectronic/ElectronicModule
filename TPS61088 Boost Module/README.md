# purchase link

[Click to buy](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4002-21223910208.11.1f1c6a4bMFKwOh&id=678460521168)

# picture display

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/PowerModule/TPS61088%20Boost%20Module/image/top%20display.jpg" width="400">

# Introduction
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This module adopts the TI TPS61088 power chip solution, with stable performance, small ripple, 10A switching current capability, and a switching frequency of about 1MHZ. The module provides two working modes: PWM and PFM, which can be adjusted by the user (the default PWM mode is shipped). High-quality tantalum capacitors and flat copper wire inductors use high-quality components to further improve the performance and stability of the module.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;When the module outputs high power, it still has the stability that most other booster modules can't match. The user uses multi-cell lithium batteries in parallel to boost the application to 5V voltage and 4A/5A output high current. A good choice, the same boost to 9V/12V voltage is not a problem, the output power can reach up to 30W, 9V, 12V voltage output, when outputting a large current, the user only needs to do a good job of heat dissipation to obtain a good belt. carrier output ripple.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Unless otherwise specified, the following parameters are tested in PWM mode.

# parameter
| module type | Switching power supply, boost power supply |
|--|--|
| Input voltage | DC2.7-12V |
| Input Current | 9A(max) |
| Output current | Determined by the input, refer to the subsequent description for calculation |
| Output voltage | DC4.5-12.6V |
| Output Power | 30W(max), need cooling measures |
| On-off level | About 1MHZ |
| Operating mode | PWM / PFM |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The following parameters are measured when the boost value is adjusted to 9V in PWM mode for user reference.

| Quiescent Current | 15-65ma (PWM mode)/200ua-600ua (PFM mode) |
|--|--|
| Output ripple | 30mVpp (no load) |
| Output efficiency | 92%(max) |
| Adjustment method | Potentiometer, boost counterclockwise |
| Module interface | KF301-5.08 |
| Module weight | 10g |
| Module size | 40 x 22 x 15mm (measured by hand, there are deviations) |

# Pin description

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Users can refer to the picture below or the silk screen on the back of the module.

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/PowerModule/TPS61088%20Boost%20Module/image/bottom.png" width="400">

| pin name | pin function |
|--|--|
| VIN | Power input positive, 2.7-12V |
| GND | Input and output negative pole, shared |
| VOUT | Positive output of power supply, 4.5-12.6V |
| EN | Boost enable switch (not for turning off the output) |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The PWM short-circuit pad on the side of the output terminal is short-circuited to PWM mode, disconnected to PFM mode, and the default is PWM mode, which can be adjusted by the user.

# About the output

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①The module is a boost module, so the output voltage adjusted by the module needs to be larger than the input voltage. After testing, it is recommended that the output voltage be higher than the input voltage by more than 2V, otherwise the output voltage is likely to be higher than the set value.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②The maximum switching current of the module is 10A, and the user is required to leave room for use within 9A.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;③The output current is determined by the input parameters. The input current should not exceed 9A, and the efficiency should be 70% (leave room for calculation). The following formula is used to calculate the maximum output current value of the module: Iout=Vin*6.3/Vout.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;④When the input voltage is too low, the output power of the module cannot be fully exerted, especially when the power supply is below 3V. Users who need higher power output should pay attention to it.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The maximum output current of the module can refer to the following table for use

| Input voltage | Output voltage | Maximum output current |
|--|--|--|
| 3V | 5V | 3.78A |
| 4V | 5V | 5.04A |
| 3V | 9V | 2.1A |
| 5V | 9V | 3.5A |
| 7V | 9V | 4.9A |
| 3V | 12V | 1.57A |
| 5V | 12V | 2.62A |
| 7V | 12V | 3.67A |
| 9V | 12V | 4.72A |

# Output ripple

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①The initial test of the output ripple of the module is below 30mVpp at 9V. It is worth noting that the ripple will increase significantly when the module is powered by an inferior power supply.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After testing, using a single 18650 battery for power supply, the ripple is basically within 20mVpp at 9V output, and the output ripple is as high as 100mVpp when using a power supply with a ripple of 0.8V at 3.5V input.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Therefore, users who have requirements for ripple should prepare a better input power supply by themselves.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②The following are the ripple parameters measured by our company under the condition of outputting 9V when using multiple 18650 batteries in parallel for user reference

| Input | Set voltage | Output voltage | Output current | Output ripple |
|--|--|--|--|--|
| Multisection 18650 | 9V | 9.04V | no load | 12.2 mVpp |
| Multisection 18650 | 9V | 9.05V | 0.5A | 22.0 mVpp |
| Multisection 18650 | 9V | 9.05V | 1A | 41.0 mVpp |
| Multisection 18650 | 9V | 9.06V | 2A | 74.6 mVpp |

No-load ripple

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/PowerModule/TPS61088%20Boost%20Module/image/No-load%20ripple.png" width="400">

1A ripple

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/PowerModule/TPS61088%20Boost%20Module/image/1A%20ripple.png" width="400">

2A ripple (with heat sink)

<img src="https://raw.githubusercontent.com/YouXinElectronic/ElectronicModule/PowerModule/TPS61088%20Boost%20Module/image/2A%20ripple.png" width="400">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The following are the ripple parameters measured by our company using the high-quality low-ripple adjustable switching power supply input. Due to the difference in the input power supply, load and measurement method, the measured results may be different from the following table.

| Input | Set voltage | Output voltage | Output current | Output ripple |
|--|--|--|--|--|
| 3V | 5V | 5.02V | no load | 20 mVpp |
| 3V | 5V | 4.99V | 0.5A | 24 mVpp |
| 3V | 5V | 4.98V | 1A | 32 mVpp |
| 3V | 5V | 4.98V | 3A | 73 mVpp |
| 4V | 5V | 5.03V | no load | 30 mVpp |
| 4V | 5V | 5.01V | 0.5A | 27 mVpp |
| 4V | 5V | 4.98V | 1A | 19 mVpp |
| 4V | 5V | 4.98V | 3A | 68 mVpp |
| 3V | 9V | 9.04V | no load | 18 mVpp |
| 3V | 9V | 8.99V | 1A | 54 mVpp |
| 3V | 9V | 9.01V | 2A | 116 mVpp |
| 5V | 9V | 9.04V | no load | 20 mVpp |
| 5V | 9V | 8.98V | 1A | 34 mVpp |
| 5V | 9V | 8.99V | 3A | 88 mVpp |
| 5V | 12V | 12.05V | no load | 18 mVpp |
| 5V | 12V | 12.00V | 2A | 90 mVpp |
| 9V | 12V | 12.06V | no load | 36 mVpp |
| 9V | 12V | 11.98V | 4A | 86 mVpp |

# Work efficiency

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①The working efficiency of the module is basically between 82 and 93% after testing. In a few cases, it has not been tested. Users can test it according to the usage.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②Under normal working conditions of the module, the smaller the pressure difference between the input and output, the efficiency will generally be improved.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;③The working efficiency of the module will decrease when the temperature rises, and the user must do a good job of dissipating heat.

# About heat dissipation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①Users can place a heat sink at the bottom of the module and directly below the chip to enhance heat dissipation. The recommended size of the heat sink is less than 24mm in length and less than 15mm in width.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②It is recommended to use cured silicone grease/silica gel to apply the heat sink evenly and then paste it. In most cases, the heat dissipation effect will be better than that of using heat dissipation tape to fix it.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;③When the temperature of the module rises, its working efficiency will drop, which will further lead to an increase in temperature. In order to prevent the module from burning out, it is very important for users to take good heat dissipation measures when working with high power/current.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;④When the input power is sufficient, the voltage drops rapidly or the voltage rises after the drop, which is caused by poor heat dissipation. In the case of large voltage fluctuations, the module has a greater probability of burning.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⑤The slow drop when the input power is sufficient is also caused by poor heat dissipation. At this time, the module will work for tens of seconds, several minutes or ten minutes after the temperature rises. The fourth point of the voltage will be greatly increased. The reason for the fluctuation is that the heat dissipation is better than that of the fourth point and it is not enough to cope with the current heat generation.

# Matters needing attention

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;①Do not touch the pin area of the bottom potentiometer with your hands or other substances with small resistance value. The contact will cause the resistance value of the potentiometer to change and cause large fluctuations in the output voltage.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;②When measuring the voltage with a large load current, please use a short/thick wire for connection (wire resistance will affect the measured voltage), or directly measure the terminal, otherwise the voltage measurement will be inaccurate.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;③The above parameters are not the limit values of the module, but the parameters indicated after leaving a certain margin. During the module test, the output power exceeds 50W under the condition that the cooling sheet is dissipating heat. It can be seen that a good heat dissipation environment is used in high-power applications. is particularly important.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;④Regarding the use of the EN port, the EN port is connected to VIN by default, and the boost mode is turned on. Connecting EN to GND is the shutdown mode. The user should pay attention to the shutdown mode. The voltage will be slightly lower than the input and will be able to output current.


