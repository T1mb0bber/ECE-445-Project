# ECE-445-Project
Repo for ECE 445 to log project progress and files 

# 1/24/2026 
Objectives: Introduce each other on the team and begin to layout project details
What was done: 
We met as a team online to discuss the underlying project that Matthew suggested. With my hardware project experience I set the expectations on how the project flow would be in terms of what amount of time it would take in making our robot. We broke into project roles and some guidelines of how we should work at as a team. Discussed stuff like meetings spots and where our schedules would meet up. I would be responsible for the PCB/electronics, Matthew for the CAD/Mechanical design/Electrical Design, and Ved for the embedded software side. 

# 1/26/2026
Objectives: Discuss design and parts strategy
What was done:
We started talking about what the overall shape that Matthew proposed initially. I was consulted with my robotics experience on certain design decisions and I discussed my thoughts with the team. We decided in this meeting on having a 4 motor design to allow for the robot to be able to move in 360 degree rotation at all times. This should allow our robot to be able to move away from a teams weapons. The biggest trade off of our design is the passive vs active weapon structure. We discussed this multiple times and came up with a few more solutions. We thought of possibly adding a middle passive wheel that would move in the center to have some dynamic movement in case a weapon tried to push out our robot. We made this a stretch goal. We started thinking about stm32 vs esp32 microcontroller and what to pick between them. Motors were discussed in terms of brushless vs nonbrushless and we found that they both were quite good. Seems as if both could work on design so we had flexibility in those options. We also pushed to create our RFA earlier so that we could get the extra credit. 

# 2/09/2026
Objectives: Begin work on project proposal
What was done:
We began talking about what was required of the project proposals. Three key things were decided in this meeting. We would opt for a esp32 microcontroller for its ease in implementing in hardware and bulit in wireless support on one of the carrier boards. I found a set of motors that I've worked with before that worked quite well. With those two important pieces decided, we can move forward in creating a comprehensive parts list and plan out the hardware sections of our project.

# 2/22/2025
Objectives: Plan more on design of robot and finalize details
What was done:
We decided to organize and prepare for the upcoming demos by making the tough decisions. This involves what type of weapon to use and what not. This is an incredibly important decision because this effects the PCB design that I am responsible for. 

# 3/4/2026
Objectives: Finalizing PCB details and work
what was done:
With all the parts and subsystems finalized we can start the process of ordering the PCB. I am in charge of it and I am planning to finish up layout details before checking DRS. As long as the design review goes well tomorrow morning we should be good to go to order. The regulators and sensors have been checked in order to ensure that they'll be the correct parts to get. Maybe consider ordering parts seperately since going through TA has been a bit tedious. Also I have access to a esp32 to work on the breadboard demo before next week. 

# 3/8/2026
Objectives: Design Review Feedback
What was done:
Professor Gruev told us to add more numerical metrics for what we want to prove in our project. We're incorporating that in a revised design document to show for the breadboard demo coming up. Ved has been working on the firmware for the breadbord demo tha is occuring next Monday of the week. So far we have wifi communication and some sort of gui to control gpios wirelessly from a external device.

# 3/15/2026
Objectives: Finalized pcb design details for upcoming order
What was done:
Coordinate with team on next steps to work on after breadboard demo. 

# 3/20/2026
Objectives: Fixing up PCB design to order 
What was done:
Telling Ved about whats features he wants on the sensor with regards to the IMU sensor as I can include interrupt pins if he desires. Double checked that my circuit designs make sense and I wouldn't be blowing up components. 

# 3/23/2026
Objectives: Double check all details of pcb design
what was done:
Checked that the motors rated stall current and the expected current draw from the motor drivers was gonna be okay. I had to add pin headers so we can attach wires to the motors Matthew found and we're gonna have to solder the wire ends onto the motors themselves. I set the logic voltage supplied to the motor drivers ICs to be less than 5v so that the current limit is set to be less than 2 A which would be the stall current of the motors chosen. This way the motors health can be preserved and they can run for a longer amount of time. I want to derate the current being sent to the motor drivers and we can also monitor this behavior by sending the CS pin to the MCU. ESP32 WROOM 32E module has three pwm motor control and up to 16 for LED control. Can use the LED PWM controller as our motor driver ICs have a set dead time whereas the PWM motor controller allows you to configure that. Since we're using a certain mode that only needs one pwm signal we can use all three motor pwms for our bot.

# 3/24/2026
Objectives: Finish Schematic
What was done:
Most of the connections are finished and footprints are found for layout. I had to spend sometime trying to understand how to hook up stuff for the ADC on the esp32 and other connections in general for the microcontroller.

# 4/1/2026
Objectives: Ordered extra parts just in case
What was done:
PCB being worked on by JLCPCB we're sort of in a waiting period in terms of the project. I pray this board works decently well and I can move on from this class. I put in a ton of time to get this to work so fingers crossed. Currently working on the individual progress report which is dued this week.