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


# July 2nd : Started and finished CAD

Today I started and finished the CAD design
To start I need to export the STEP file from KiCad (PCB Editor) to fusion. This allows me to accurately get the dimensions of the PCB and design appropriately.
Once in KiCad I can click on file and then export as step and be brought to this window
<img width="712" alt="image" src="https://github.com/user-attachments/assets/03eb7ef4-6582-4144-b8e0-5f4d6f87df66" />

I left the settings as default and exported the STEP File
After importing it into fusion it looks something like this

<img width="859" alt="image" src="https://github.com/user-attachments/assets/d9c089a6-b7fb-47c4-bb72-2f2b75aa9577" />

After importing the PCB I can create a base outline around it that looks something like this

<img width="962" alt="image" src="https://github.com/user-attachments/assets/3f01f351-c68d-420e-8efa-a9833a6f91c4" />

Here is the base with the PCB

<img width="942" alt="image" src="https://github.com/user-attachments/assets/acae7851-9c2f-4f59-ace3-cf957be9114d" />

I then created an outline for the top roof housing the ESP and holes for the pads

<img width="957" alt="image" src="https://github.com/user-attachments/assets/8eeeb65d-727c-435c-a7b2-f4857dafd0ee" />

Here is the roof with the PCB

<img width="964" alt="image" src="https://github.com/user-attachments/assets/819491dc-a944-4c82-8f68-77b9a80d4f83" />

And finally here is the completed case

<img width="983" alt="image" src="https://github.com/user-attachments/assets/517a29dd-1852-4f80-9ca9-1ad49330497a" />

Now after building all of this I realised I made a crucial mistake. I left out the holes for the layer switch buttons here

<img width="318" alt="image" src="https://github.com/user-attachments/assets/1c930fd3-50c7-4caa-a9e9-35a2013dfbbe" />

To fix this I just created another sketch and ended up with something like this

<img width="258" alt="image" src="https://github.com/user-attachments/assets/ea9bae95-7a87-4f3b-9e51-fc1e1ce10012" />

After that I added Fillets to everything to round everything and was left with something like this

<img width="892" alt="image" src="https://github.com/user-attachments/assets/b22b5e05-868b-4534-839a-fd75dcf00708" />

After this I realised I also forgot the holes for the ESP and headphone jack so I created a simple hole sketch like so

<img width="524" alt="image" src="https://github.com/user-attachments/assets/521e10c1-8f49-41bf-b6b4-7bb4a7e8be86" />

After extruding I was left with something like this

<img width="813" alt="image" src="https://github.com/user-attachments/assets/423f363e-a9ba-4d92-88ed-f8ad40f7f202" />

I can the fillet everything to get a nice rounded finish

<img width="890" alt="image" src="https://github.com/user-attachments/assets/29954f33-1ff4-4790-ac6d-d465044c1415" />

I repeated the same steps for the headphone jack and SD card and was left with the finished case

<img width="726" alt="image" src="https://github.com/user-attachments/assets/b843bbd4-277d-4f68-8951-5f0a5f28ff52" />

<img width="1006" alt="image" src="https://github.com/user-attachments/assets/97cca855-5a98-4388-8a1a-eba57551ec2a" />

Thats it!, The entire case + PCB is complete! To print it since it has holes it is made in 2 parts to glue together so it requires minimum supports!







