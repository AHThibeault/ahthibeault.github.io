---
title: 'PCB Design Projects'
date: 2023-05-10
permalink: /posts/PCB-Design
tags:
---

I took Professor Eric Bogatin's Practical PCB Design and Manufacture course during my final semester at CU Boulder. This course was lab-based and covered industry accepted best PCB design practices for risk management, test, signal integrity, power integrity, manufacturing and reliability, while meeting cost and schedule goals. Using Altium, we completed four board design projects throughout the course of the semester, along with numerous labs covering how the principles of circuit theory, electromagnetics, materials science, and practical manufacturing constraints drive the design trade-offs in circuit board design and manufacture. My four board design reports are included on this page as PDFs. The semester culminated with our most complex board design project, Board 4, in which I designed a 4-layer instrument droid board with a microcontroller and data acquisition system.

## [Board 1](/files/Thibeault_brd1FinalBoardReport_2023-02-20.pdf):
A simple and functional design (555 timer driving several LEDs) to gain experience with the entire board design flow, from simple sketch, to layout, to assembly and test. In this board design I demonstrated the advantages of using isolation switches, well-placed test points, decoupling capacitors placed to minimize inductive loop lengths, and a continuous ground plane, among other features to maintain signal integrity, make the bring-up process easy, and enable easy debugging.

![board 1 layout](/images/brd1layout.png)

![board 1 pcb](/images/brd1pcb.png)

## [Board 2](/files/Thibeault_Board2Report_2023-03-12.pdf):
A board to demonstrate how good and bad layout practices affect the amount of switching noise in a PCB, and to put into practice the best measurement techniques for measuring switching noise. In this board, two hex inverters with resistive loads at their outputs are driven by a 555 timer signal. The layout of each hex inverter is implemented differently, one with good design practices (decoupling capacitor placed close to the IC and a continuous ground plane), and one with bad design practices (cap far from IC and individual ground traces routed through a common path). I was able to show significant improvement in switching noise with good design practices.

![board 2 layout](/images/brd2layout.png)

![board 2 pcb](/images/brd2pcb.png)

## [Board 3](/files/Thibeault_Board3Report_2023-04-16.pdf):
A "Golden Arduino" which meets the same connectivity specs as the commercial Redboard Arduino Uno, but has features for better noise control, assembly, test, and bring up. I was able to design a board that reduced power rail noise and ground bounce and cross talk noise to 50-70% of that of a commercial board, along with reducing near field emissions to 29-43% of that of a commercial board.

![board 3 layout](/images/brd3layout.png)

![board 3 pcb](/images/brd3pcb.png)

## [Board 4](/files/Brd4_Thibeault_2023-05-07.pdf):
A 4-layer instrument droid board with a microcontroller and data acquisition system. The microcontroller is bootloaded as an Arduino Uno, and connectivity specs are kept consistent with the commercial Arduino Uno, enabling the use of this board as an Arduino Uno outside of its capacity as an instrument droid. The instrument droid is designed to measure the Thevenin output resistance of any supply. The purpose of this board was to pratice using a 4-layer design in order to optimize performance by minimizing cross-unders that create gaps in the ground plane, as well as demonstrating the instrument droid which will reveal the limitations of power sources inherent in their Thevenin resistance. My design successfully performed its instrument droid function and demonstrated significantly reduced noise characteristics than the previously designed 2-layer 'Golden Arduino' and particularly from the commercial Arduino, with switching noise reduced to 20-70% of that on the commercial board.

![board 4 layout](/images/brd4layout.png)

![board 4 pcb](/images/brd3pcb.png)
