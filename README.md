# ec11_skirt
## A snap-in skirt to secure EC11-style rotary encoders in a keyboard plate.

The [Tangent Space Basis keyboard](https://www.instagram.com/_tangent_space_/) uses Alps EC11 (and compatible) rotary encoders to provide programmable continuous inputs for users.  In order to provide easy tweaking, replacement, and assembly, we used Mill-Max sockets to allow the encoders to be hotswapped by users in a similar way to how hotswappable MX key switches work.

This means that the encoders can be replaced without soldering, but the socketed pins and unsoldered supports result in a much weaker connection between the encoder and the PCB.  The official Tangent Space keyboard durability tester (a 2 year old toddler who loves twisty knobs) was able to easily dislodge the encoders from the PCB, so a better method of securing the encoders was required if we want to ship a keyboard with hot swap encoders.

Hot-swap MX switches mitigate this weakened connection by providing an additional mechanical connection by snapping into the keyboard plate, a rigid piece of material (usually metal, occasionally plastic) that sits 3.5 mm above the PCB.  EC11 encoders do not have a mechanism to snap into this plate, and also sit higher than 3.5mm (the encoder base sits about 4.5mm above the PCB) and thus will collide with a standard 2 dimensional plate if the cutout for the encoder isn't large enough to clear the base of the encoder.

Additionally, the pins for encoders extend outside the footprint of the base, and if we want to enable users to swap encoders without dismantling the rest of the keyboard we need a plate cutout that is large enough to pass the complete footprint of the encoder through.

To fix this, we decided to design an additional part that would secure the EC11s to the plate.  The hot swappable PCBs have standoffs to secure the PCB and the plate together at a fixed distance, so all this part needs to do is secure the EC11 from moving on the X/Y plane.  We wanted it to operate like a keyboard switch, and let users use their existing switch pullers to remove it from the plate.

Our solution:

<img src="images/ec11_skirt_render.png?raw=true" alt="EC11 Skirt Render" width="600" height="600">

Because the fit of these skirts is extremely important, they require a specific keyboard plate cutout.  This plate cutout was designed to fit into a 19.05mm radius circle, so an encoder could be added anywhere in a keyboard grid without requiring extra space.

The first version of the encoder requires a 15.5mm by 15.5mm cutout, with a 5mm radius fillet on each corner.

<img src="images/ec11_skirt_cutout.png?raw=true" alt="EC11 Plate cut">

We had several of them SLA printed in Form Tough and Form Durable.

<img src="images/skirt_plate_photo.png?raw=true" alt="EC11 skirt in plate">

<img src="images/skirt_in_bezel.png?raw=true" alt="EC11 skirt in high profile bezel">

We found the Form Durable provided a more secure fit, and we're planning on printing more in that material or experimenting with similar 3D Systems materials.

This version of the encoder fits true Alps EC11 encoders as well as Bourns PEC11L encoders.

For the next iteration, we're planning on adjusting the sizing a bit to allow looser manufacturing tolerances.  A .1mm offset of the surfaces that connect to the encoder will probably provide a more reliable fit (it's a little too tight right now).

We'd also like to find a way to make the plate hooks a little tougher, so they're a little more rigid and grab the plate a little tighter.

If anyone tries these in their own board, please let us know!  We'd love to get more feedback on the design and iterate towards a better solution.
