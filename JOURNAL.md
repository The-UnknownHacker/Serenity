---
Title: "Serenity"
Author: "Aarav J"
Description: "Serenity is a drumpad that uses copper touch panels!"
Created_On: "24/6/2025"
---

# June 24th: Started choosing components and integrating them with the PCB

I started to choose the components that I am going to use - /
First I decided on using the Xiao ESP32-s3 board but now I might use a normal ESP32-s3 devboard as I need more gpio
The parts I have decided for now are

- ESP32-s3 devboard
- Micro SD Card Slot
- Headphone Jack
- MAX98357A Audio DAC
- Everything will be powered by the ESP's USB C port

I also started to wire up most of the circuit and I think I have finished the first version of the schematic. 
This is a rough schematic and I will need to double check if it fully works or not.
![Day 1](https://raw.githubusercontent.com/The-UnknownHacker/Serenity/cf86a7b0c3918c50002f7faede01b7a9038a4543/Day%201.png)


**Total time spent: 8h**


# June 26th : Assigned some of the footprints and started the PCB with rough routing

Today I started a rough PCB design and diagram to visualize the basic design.
As of now my design is still missing key resisistors and capacitors and is not in working shape just yet (just a mockup)

![Day 2](https://github.com/The-UnknownHacker/Serenity/blob/305006b9234b0b8d88c552c5b0c2ab27f9807b0b/Day%202.png)


**Total time spent: 4h**


# June 28th : Assigned all the footprints and finished the PCB outline

Today I finished choosing all my parts and assignigning all the footprints + alignment. I then alligned all the parts on the PCB and chose a design. 

I had some difficulty in getting the copper pad loaded onto the PCB but I figured out that I can import a black square into kicads image translator and then convert that to a footprint. From there I can then draw out a trace from the copper pad and assign the net to one of the digital connector pins on the ESP32.

At the end I ended up with something like this
<img width="725" alt="image" src="https://github.com/user-attachments/assets/59f76b79-f993-45c6-be18-eb74634e047d" />

And for the PCB

<img width="924" alt="image" src="https://github.com/user-attachments/assets/6dd39bc8-0861-498b-8ff0-6e6bf950354d" />


Now it was time to begin the routing 😭

I spent a good 2 hours on this and it was fairly challenging as I had to be careful with the copper pads and not to short anything

<img width="1038" alt="image" src="https://github.com/user-attachments/assets/6798459e-b35d-46fc-9a55-c56bd6061f6e" />


After running a DRC it showed a couple errors relating to the trace shorting a pad. This is a known error and isnt a problem as the trace NEEDS to short the pad to make a connection. Otherwise the PCB is fully clear. At the start I experienced a trace cutoff error meaning that the trace was too close to the edge of the board and this was fixed by just extending the board length


<img width="686" alt="image" src="https://github.com/user-attachments/assets/7ef4ccfc-9a46-494c-bff6-7fa7de284d86" />

**Total time spent: 6h**

