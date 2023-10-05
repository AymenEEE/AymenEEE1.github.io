---
layout: project
type: project
image: img/LED_beacons.jpg
title: "Solar energy LED beacons"
date: 2023-05-01
published: true
labels:
  - LED
  - Switch Mode Power Supplies
  - C++
  - Python
summary: "This project is focused on using solar energy to create an energy grid capable of powering on 3 LED's. "
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>
<h2> What </h2>
Powering a grid using the sun is not as straightforward as it initially seems. This is because the voltage that a solar panel outputs is proportional to sunlight intensity, which is rarely stable (especially in the UK!). Consequently, we need a way of drawing varying amounts of power based on how much is available from a panel. 
One solution is using an SMPS (Switch-Mode Power Supplies), which can draw different voltages (hence currents) based on the duty cycle of a PWM signal. The duty cycle is proportion that a signal with period T seconds is on (or HIGH), and varies between 0 and 100 percent.



<h2> Equipment </h2>
<ul>
  <li>5 volts, 230mA solar panel (x3)</li>
  <li>Buck/Boost SMPS device</li>
  <li>18V, 0.25F Capacitor</li>
  <li>Buck SMPS with adafruit microcontroller (x3)</li>
  <li>Red LED</li>
  <li>Blue LED</li>
  <li>Yellow LED</li>
  <li>Sun?</li>
</ul>


```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```
