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

I thought of a fun (and safe) way to utilise and demonstrate PID controllers in action, and this is what came across. It moves like a see-saw but the force is only on one side. This is harder to work with than a system with two motors opposite to each other, as we are relying on gravity to pull down the stick when we want it to descend.

Most of the process involved designing the physical aspect which includes the stand, pivot and the freely rotating stick. The rest of it was placing the components on and coding the algorithm into a micro-controller.
I used screws and brackets to stabilise the stands, and two ball bearings where the shaft inside the stick goes between.
This is what it looked like:

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>


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
