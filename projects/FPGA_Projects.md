---
layout: project
type: project
image: "img/FPGA/thumbnail.png"
title: "FPGA Projects Collection"
date: 2022
published: true
labels:
  - Digital circuit design
  - Intel Quartus
  - SystemVerilog
    
summary: "This page shows a brief summary of my FPGA projects which includes 7-segments display, clock dividers and linear feedback shifts"
---
<h2>Lab 1</h2>
  <h3>Segment displays</h3>
  Driving a segments display is rather simple. All we have to do is create a look up table that corresponds to the individual segments and we're all good .
  

  <div class="text-center p-4">
  <img width="400px" src="..img/FPGA/Segment.png" class="img-thumbnail" >
  </div>
      
  <iframe width="560" height="315" src="https://www.youtube.com/embed/sjViU3GZsU4?si=7ITH9VzRnV-XH2_N" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

  The same process is repeated for three displays. Each display can show up to 4 bits. Note that we are displaying the binary numbers as hexadecimal on the segment displays. (The video below has been reflected for some reason).
  
  <iframe width="320" height="560" src="https://www.youtube.com/embed/oSAhVVj67Rg" title="Three Segments" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  
<h2>Lab 2</h2>
  <h3>Counters</h3>
    This counter starts counting whenver en is pressed. The KEY button is AND'ed with the main system clock, and is wired to the enable port of the CTR module.
    

  <div class="text-center p-4">
    <img width="400px" src="..img/FPGA/counter.png" class="img-thumbnail" >
  </div>
  
  <h3>Linear feedback shift registers</h3>
  Linear feedback shift registers allow us to generate a sequence of seemingly random numbers. For this reason, they are called "pseudorandom" as the sequence is completely predictable.

  <div class="text-center p-4">
    <img width="400px" src="..img/FPGA/LFSR.png" class="img-thumbnail" >
  </div>
  
<h2>Lab 3</h2>
  <h3>PWM generator</h3>

  <div class="text-center p-4">
  <img width="400px" src="..img/FPGA/PWM.png" class="img-thumbnail" >
</div>

  <ol>
    <li>The ramp generator produces a Sawtooth wavefore</li>
    <li>The data register updates its output at rate of the frequency of the pulses outputted from clktick module.
    <li>The sawtooth wave generator is connected to the negative input of the digital comparator, hence the comparator only outputs 1 if the wave is smaller than the       positive input data_in</li>
    <li>Increasing data_in increases the duty cycle of the digital comapartor's output</li>
  </ol>
