# Spot-Welder
This project was inspired by something I found on the web that I wanted to expand upon.

The original site was http://www.kerrywong.com/2017/06/18/dual-purpose-spot-welder-with-pulse-duration-control/

Like most hobbyists or design engineers, I have a curious nature and usually have a dozen projects all going at once, this seemed like yet another neat project to add to the list.

Having recently updated our kitchen appliances I just happened to have an old microwave oven that was destined for the landfill. So the donor for the transformer was sitting in my garage.
I tore the oven apart to find a huge power transfomer which is used to power the magnetron (device used to create the RF waves that cook the food in the microwave).

With the transformer now scavanged I had the heart of my new spot welder! 

I like Kerry's project but being an electrical engineer myself and loving microcontrollers the way I do I thought upgrading the controller was in order.
I quickly sketched up a schematic in Altium using a PIC18F26K40, 2x16 LCD, rotary encoder, foot switch, isolated power supply and a SSR(Solid State Relay).

I had recently acquired an old piece of test gear that was housed in a nice instrument case which was used for the spot welder as well. 

Sparking up Altium again I did a PCB layout. With parts being so small nowadays it just isn't easy for me to breadboard projects anymore. I used PCB Way in China to manufacture the PCB's. They do a great job, are low cost and I usually have boards in about a weeks time. 

When the PCB's arrived I started to populate one and test my code. Hmm . . the SSR would never fire? I found an error in the MOSFET symbol . . . so I mounted the MOSFET upside down which swapped pins 1 & 2 thereby fixing my mistake. Everything was now working! I use the rotary encoder to change the timing from 100mS to 1200mS in 100mS increments. Once the correct time is set press the encoder to save this time into EEPROM so it will remember for the next power cycle. Pressing the footswitch starts a spot weld cycle. Next I added some connectors for the footswitch and the welding cables. 

My next project to wrap this one up is the handheld tweezer type welding probes. 

I am experimenting with nixie tubes and my goal is to eventually make one. The spot welder will be used to attach the internal wires of the nixie to the pins of the tube itself. Because the tube will require extreme heating a simple solder joint won't suffice here. One avenue I am also looking into is the use of plastics instead of glass since the nixie tube never gets very hot under normal running conditions. 
