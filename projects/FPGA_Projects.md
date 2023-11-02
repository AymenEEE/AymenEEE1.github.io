---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "FPGA_Projects_Collection"
date: 2021
published: false
labels:
  - Digital circuit design
  - Intel Quartus
  - SystemVerilog
    
summary: "This page shows a brief summary of my FPGA projects which includes 7-segments display, clock dividers and linear feedback shifts"
---
<h2>Lab 1</h2>
  <h3>Segment displays</h3>
  <p>Driving a segments display is rather simple. All we have to do is create a look up table that corresponds to the individual segments and we're all good </p>
  
  <iframe width="560" height="315" src="https://www.youtube.com/embed/sjViU3GZsU4?si=7ITH9VzRnV-XH2_N" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

  <p> The same process is repeated for three displays. Each display can show up to 4 bits. Note that we are displaying the binary numbers as hexadecimal on the segment displays. </p>
  -- insert image & video
<h2>Lab 2</h2>
  <h3>Counters</h3>
    <p> This counter starts counting whenver en is pressed. The KEY button is AND'ed with the main system clock, and is wired to the enable port of the CTR module.</p>
    -- Insert img
  <h3>Linear feedback shift registers</h3>
    <p>Linear feedback shift registers allow us to generate a sequence of seemingly random numbers. For this reason, they are called "pseudorandom" as the sequence is completely predictable</p>
    
    
<h2>Lab 3</h2>
  <h3>PWM generator</h3>
