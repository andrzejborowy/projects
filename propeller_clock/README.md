# Propeller clock

I were studying on Warsaw University of Technology. Newar the end of my studies I decided to prepare my diploma work. I didn't want to just describe some problem. It was too obvious. So I choosed to "make a thing" which would work. At that time I was fascinized about proppeler clocks which I have seen in web. 

It passed couple of years, but I'll try to describe my construction.

## Way of propeller clock works

Fundamentals of propeller clock are based on inertion of human eye. If some point light is moving circle quite fast, there is possibility for human to see this as spinning circle. But speed must to be saved.
If light will comes with some breaks, it will be visible as dots.
Then If we use not one point light bui many of them it is possible to see some fun shapes.
Back to inertion of human eye - there is perfect example of this effect. Newton Circle. This is multi-color circle. With enough high rotation it will become white for observer.

![image](https://github.com/andrzejborowy/projects/assets/72155321/96cdd1f2-7bff-4be8-96fa-5462c1fc04ff)

Simplified explanation of how propeller clock works is here:

![image](https://github.com/andrzejborowy/projects/assets/72155321/192a8bd9-7989-4d1e-bb7f-2e778bed06e7)

## Mechanical

I started building propeller clock from the mechanical part. Some of this design was based on my imagination, other part was based on parts that i had.
Construction should have to be simple because main aim of diploma work was to make it working and presenting effect of light, not beauty of mechanics.
Main construction were made of painted black plywood. Others elements were bolted or glued to it.

![image](https://github.com/andrzejborowy/projects/assets/72155321/31bab016-a3ac-4016-94d3-24f258f32e6d)
![image](https://github.com/andrzejborowy/projects/assets/72155321/411dff9a-f274-4758-b85d-060d8a5ed3d1)

All models were made in Autodes Inventor 2015.


## Electronics

Electronics part was the biggest part of my diploma work. Because of that I decided to divide this chapter.

### Wireless power supply

When I was designing this clock, one of this problem was to power supply main rotating board. Every motor brush would generate some inertia for spinning so main effect of propeller clock might to not be visible or hard to see with good luck. Because of that I decided to use wireless method of transfering power. First tries were based on transfering power to power supply little light bulb. It was more experimental.

![image](https://github.com/andrzejborowy/projects/assets/72155321/ff668b45-fb61-4af9-aa63-e67ac4556a64)

For driving transistor used to generate signal for coil, i used Arduino Mega2560.

![image](https://github.com/andrzejborowy/projects/assets/72155321/62181971-4213-4d6e-a1f0-89480d6c2ab7)

After method worked, it was time to place it on something. And it has been done on rotor of fan. I used some paper tape for some reason. It didn't looked nice but it worked well. Distance between coils were about 1mm.

![image](https://github.com/andrzejborowy/projects/assets/72155321/02352818-3917-43d7-8e60-36bc88ac0bd0)
![image](https://github.com/andrzejborowy/projects/assets/72155321/2a74b774-9922-4175-8eb0-56a6e77993d7)

### LED's drivers

I decided to use RGB SMD leds. as many as I can. It occured that it is possible for me to use 24 leds (each housing had red, green and blue inside). In this case I had to drive 72 leds as fast as possible.
Because of that I used dedicated led driver SCT2024CSSG.

![image](https://github.com/andrzejborowy/projects/assets/72155321/bd4b3bb7-e110-4e68-938f-a852249b7399)

 To be precise, five of them...

![image](https://github.com/andrzejborowy/projects/assets/72155321/d9a06763-7fe3-4961-a342-8a325f8ad6c3)

All of driver's communication were connected in serial. It was a must to sent one full line for driving even one led. After sending the line, microcontroller sent latch signal which force to bring value from bufor to their outputs on leds.

### Microcontroller

In my diploma work I used Atmega 88PA. Decided price, MOQ and simple way of programming. It needed only one USBASP programmer which was very cheap at that time. So I bought one for this project.

### PCB

I designed two PCB's for this project fully in KiCad. First of all KiCad is free. Good reason i thought. Second of all it has really good support in web on on all kinds of forums groups.
First board was for powering supply. It has generator on it wit MOSFET type N transistor to drive coil (or I should to say "air transformer").

![image](https://github.com/andrzejborowy/projects/assets/72155321/c30f0c61-620e-4615-aa81-df5c51b99cd2)


The second one had every spining element on it. Leds, led's drivers, microcontroller, crystal, connectorl, etc. 

![image](https://github.com/andrzejborowy/projects/assets/72155321/6baf6335-229c-4961-ba15-63d443953a0a)

### Manufacturing PCB's

I didn't wand to order those PCB's somwhere abroad, pay a lot of money and wait months. I used thermotransfer method to make them on my own.

![image](https://github.com/andrzejborowy/projects/assets/72155321/c4d74349-c990-40c7-a725-4445c3bb1988)
![image](https://github.com/andrzejborowy/projects/assets/72155321/9bd86be3-f19b-439a-85c6-d04b0f41f67d)

## Programming

I don't know what to say here. My programming skills then and now are different. Very different. To sum this chapter up - whole program was written in C and was using essentials of programming (some delays, working on registers - nothing really "fancy"). For programming I used Arduino IDE - at that time it was simpler to me than using terminal. I don't know why. Today me and the "Mister Terminal" are good friends.

After I made some firmware there was time for some first tries...

![image](https://github.com/andrzejborowy/projects/assets/72155321/c0facd87-0ec2-494b-85f0-55119a76cf40)

## Final results

I made a propeller slock by myself. It sounds proud even now.

![image](https://github.com/andrzejborowy/projects/assets/72155321/294547bd-e691-4690-b91f-93eec94ef9c0)
![image](https://github.com/andrzejborowy/projects/assets/72155321/6de6364b-3267-485c-be62-a98982921a05)

https://github.com/andrzejborowy/projects/assets/72155321/5c371729-a9a9-48e9-8715-63acbc4fcbe6







