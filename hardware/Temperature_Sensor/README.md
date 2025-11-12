# Temperature Sensor
The Vital Signs Monitor uses a temperature sensor which measures rectal and skin temperature.
General Electric, Mindray and Welch Allyn use a 2.252 kΩ NTC sensor at 25°C.

## NTC Sensor
Negative Temperature Coefficient Thermistor (NTC) is a type of temperature-sensitive resistor where <b>the resistance decreases as the temperature increases</b>.

### PS222J2 NTC Sensor
 PS222J2 is a NTC sensor which has following specifications:

* Resistance at 25 °C: 2.252 kΩ 
* Resistance tolerance: ± 0.1 °C
* B0/50: 3890 K
* Operating Temperature: -80 °C ~ 150 °C
* Power-Max: 30 mW

The resistance–temperature relationship:

$$
R(T) = R_{25} \cdot e^{\Beta(\frac{1}{T}-\frac{1}{T_{25}})} 
$$
<div align="center">
    <img src="img/NTC_Model.jpg" alt="NTC Model" width="350" height="250"> <figcaption><b>Figure 1:</b> NTC thermistor resistance–temperature model.</figcaption>
</div>
<br>
This design considers a range of 10 °C to 50 °C, so it uses a resistance of 820.73 Ω to 4.495 kΩ
<div align="center">
    <img src="img/NTC_Model2.jpg" alt="NTC Model" width="350" height="250"> <figcaption><b>Figure 2:</b> NTC thermistor resistance–temperature model. <br> (Range of 10 °C to 50 °C).</figcaption>
</div>

<br>

More Information: \
[Datasheet PS222J2](https://www.littelfuse.com/assetdocs/littelfuse-leaded-thermistors-standard-precision-ps-datasheet?assetguid=f2c5cde0-806d-4632-bdd3-5e56183e2fd4)

## Hardware Designs
I plan to design three different circuits, each with distinct components, cost, and noise tolerance.

Therefore, it is also necessary to review the characteristics of the RP2040 ADC.

### SAR ADC in the RP2040
The SAR ADC has the following features:
* The ADC has 12 bits of resolution.
* Capturing a samples takes 96 clocks cycles.
* The ADC input has a capacitance of approximately 1 pF.

More Information: \
[Datasheet RP2040](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)

### Voltage Divider with RC Filter

### 



# References
1. Raspberry Pi Ltd. (2025). RP2040 datasheet: A microcontroller by Raspberry Pi [PDF]. https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf
2. Littelfuse, Inc. (2025). PS222J2 leaded thermistor – standard precision PS series [Datasheet]. https://www.littelfuse.com/products/sensors/temperature-sensors/ntc-discrete-sensors/standard-precision-ps/ps222j2