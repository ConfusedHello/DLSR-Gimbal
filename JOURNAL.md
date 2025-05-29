---
title: "DLSR Gimbal"
author: "ConfusedHello"
description: "A DIY Gimbal for a DSLR Camera!"
created_at: "2024-05-26"
---


## May 29th - Git commit
Finally ready to move onto some designing! After some more research I landed on the GM5208-12 motor. It's the standard motor from iPower's GM5 lineup, albiet not particularly cheap at approx $60AUD each ($38.66USD) it's the lineup made for gimbals and suits the job well. I'll add these to the newly-made [BOM](/src/frame/README.md).

After a quick search online, I was able to find the dimensions for the motor online
![Image of the dimensions of the GM5208 gimbal motor](/assets/GM5208_12_Dimensions_Reference.png)

Next I deep-dived into the [STorM32 BGC project](https://github.com/olliw42/storm32bgc/), after looking through the documentation as well as the schematics of the components I settled on the T-STorM32 architecture and created the first draft of the gimbal layout and how it would be wired up
![Draft of the gimbal design with labled components](/assets/Gimbal_Layout_Initial.png)
![Draft of the gimbal wiring](/assets/Gimbal_Layout_Wiring_Initial.png)

After some more planning for how the motor controllers would be mounted..
![Draft of the motor controller mount](/assets/Gimbal_Layout_Motor_PC_Mount_Initial.png)

And for some quick ideas:
- CF tubes instead of plates = cheaper
- 90° joins using cut CF plates and screws
- custom joystick + button pcb/mount

**Time spent: 6hrs**


## May 28th - Git fetch
Spent most of today finishing off my hackpad. However, in the hour and a bit I spent today researching, there was a big discovery. The STorM32 project, a 2013 gimbal board designed... for drones. After some extensive research, I only found 2 examples of this board being used for a full-frame camera gimbal. The good news? It's **open source**, meaning I now have an excellent foundation to build upon for the controller side.

I now have the confidence to begin designing the frame, tommorrow I will begin by choosing a motor, then looking into designing an encoder PCB/frame for it.

**Time spent: 2hrs**


## May 27th - Git clone
A lot more research research on existing DIY Camera Gimbals today! The main takeaway is that the manjority are actually **two-handle gimbals**. Why is that?

Once you've moved from light cameras such as a phone or action camera, they're a little difficult to hold in one hand, particularly if they're balanced *above* the level your hands are at (you can think of this like trying to hold a metal pole at a 45° angle in front of your body). Now when you switch to not only being able to hold it directly *below* your hand-level, as well as using *two* hands, it's a whole lot easier.

Spent today looking at basically all the existing DIY gimbals and their components, in summary:
- For non-action camera gimbals, two-handle is the way to go
- The MCU/ESC board that most projects use, the SBG32 (or an older version) are MUCH too expensive (approx. $300 AUD for one), so I'll have to design my own.

Will begin component selection (primarily the motors to use, as well as what the frame will be made of) tommorow to decide on the requirements for the MCU/ESC. This should be slightly easier than going at it with no experience due to some prior experience designing drones.

I'll also use this time to note, the name of the project isn't exactly accurate as I'm designing this for a mirrorless camera... Full Frame Camera Gimbal or something of the sort may have been a more accurate name. Looking forward to tomorrow!

**Time spent: 3hrs**


## May 26th - Init
Today was primarily determining the viability and establishing the general idea for the project.

As I'm somewhat of a hobbyist photographer, I've considered the idea of building my own camera gimbal for videography as even second-hand on Facebook Marketplace they can be a few hundred AUD. However, I've never particularly had the opportunity (or funds) to attempt it ~~spent all my money on cameras~~.

After some debate and sanity-checking my knowledge of a few DJI gimbals, we can now categorize the majority of consumer camera gimbals as either **single-handle handheld gimbals** or **two-handle handheld gimbals**. Images below, respectively:
![Image with showing two different types of camera gimbals](/assets/Gimbal_Example_Forms.jpg)

Now an observant individual may have realised both these form factors have one thing in common. They both stabilise the camera with 3 axis - **pitch**, **roll**, and **yaw**. Diagram by Horia Ionescu below:
![Diagram of 6 Degrees of Freedom](https://upload.wikimedia.org/wikipedia/commons/f/fa/6DOF_en.jpg)

So while single-handle gimbals are easier to use for phones and your standard cameras (such as the Ronin S supporting up to 3.6kg), you'll never see one on a film set where wheeled steadi-cams, sholder rigs, and other massive gimbals are used.

So what do I actually need? (Hint: this is where we establish our *scope*) Personally, my camera setup without a cage weighs approximatly 1.2kg, well under the Ronin S' 3.6kg limit or the Ronin 4 Mini's 2kg limit - so a single-handle gimbal should do fine. We'll need it to handle somewhere around 2kg, so let's set that as our target.

To summarise:
- I will be desiging a 3-axis, single-handle handheld gimbal
- The gimbal must support up to 2kg

Tomorrow's journal will probably not be as detailed as this one, definately spent too long on it.

**Time spent: 4hrs**
