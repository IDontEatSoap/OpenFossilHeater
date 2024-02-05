# OpenFossilHeater
Open Software to control Fossil-fuel (Diesel, Gasoline, Kerosene, etc) based heaters


Chinese-cloned Diesel heaters are very popular, they work OK, and extremely simple.
They’re made of two main modules. The mechanical module, and the software to control it.
Mechanically, the chines clones work satisfactorily.
Mechanically, they’re a simple clone of an old German-made design. 
Mechanically, some clones are good, others are bad; but most are good enough for the price. 
Mechanically, they have 4 components: 
1) 1 pump
2) 1 glow-plug
3) 1 thermostat
4) 1 DC motor to control airflow (with one shaft and two turbine fans, one mounted inside the unit, other outside)

But that’s where the good part ends. Their control software and hardware is all over the place, and they’re all mostly junk.

This project aims to close that gap. We’ll create software and hardware to control these units.
The ultimate goal is to have software and hardware that is extremely extensible, and controls the heater in my motorhome using the quietest fans, in all conditions and altitudes, and communicates via MQTT and UDP to a control app and home automation software.

Project milestones, outlined in versions, are:

V0.0XX: 
This is basically mocking around. Lab code, junk everywhere. We might make a DC motor move and a relay ignite a glowplug. We might see how much current a glowplug draws, and the temperature that Diesel and Gasoline ignite.
We might post experiments, we might not. Who knows…

V0.1XXX
We’re getting somewhere. At this point, we should have one static breadboard hazardously plugged into an actual heater, and who knows, we might have ignition and stable combustion. Everything is probably static spaghetti code here.

V0.19
This is probably, mostly functional. We might move one number, and get temperature to go up and down. Wow, we might even have an external thermostat! 
V0.40
We have software that reliably ignites, maintains pumping frequency to keep the unit chamber in one desired temperature, and controls external temperature; too.
V0.69
We have reliable Diesel ignition, stable pump, controls unit temperature based on intake temperature and setpoint temperature. We will have PWM intake and outflow fans. We might control multiple fans. 
This is probably the first DYI PCB, and I might be happy here. The goal is to reliably control my everyday heater in my future motorhome. It will have a custom enclosure, and multiple fans. 


V1.0
This might be some sort of optimized version of the shitty spaghetti code we started with. But the software will be reliable at this point, and our first v1.0 PCB will be extensible enough for future versions.

The PCB should support:
Multiple FAN controls, both DC and PWM.
Robust pump interface, with SSRs and things.
Stable voltage control – hopefully from a very wide range (12 to 48v?)
Robust current and temperature measurement ICs. 

V2.0
This might be a complete code refresh from V1, aimed making the platform easier to expand and extend. Multiple pump types, thermostat, glow plugs, airflow, fuels, and etc might be supported in the future. This version aims to make those modules easy to mix and match.

V3.0
Super polished software, that can control any fossil fuel lamp from the 1500’s all the way to 2500. Just bang the rocks together, folks.

