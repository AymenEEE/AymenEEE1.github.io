---
layout: project
type: project
image: img/LED_beacons.png
title: "Balancing Drone"
date: 2023-09-28
published: true
labels:
  - Brushless motor
  - Arduino
  - C++
summary: "This balancing drone uses an arduino integrated with an mpu6050 sensor and a brushless motor to control its angle using a PID algorithm."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

The aim of this project is to examine and demonsrate how the proportional, integral and derivative constants affect a system's response. The challenge here is to achieve as smooth and quick response as possible using only one motor.


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

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
