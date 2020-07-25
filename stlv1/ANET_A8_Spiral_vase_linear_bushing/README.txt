                   .:                     :,                                          
,:::::::: ::`      :::                   :::                                          
,:::::::: ::`      :::                   :::                                          
.,,:::,,, ::`.:,   ... .. .:,     .:. ..`... ..`   ..   .:,    .. ::  .::,     .:,`   
   ,::    :::::::  ::, :::::::  `:::::::.,:: :::  ::: .::::::  ::::: ::::::  .::::::  
   ,::    :::::::: ::, :::::::: ::::::::.,:: :::  ::: :::,:::, ::::: ::::::, :::::::: 
   ,::    :::  ::: ::, :::  :::`::.  :::.,::  ::,`::`:::   ::: :::  `::,`   :::   ::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  :::::: ::::::::: ::`   :::::: ::::::::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  .::::: ::::::::: ::`    ::::::::::::::: 
   ,::    ::.  ::: ::, ::`  ::: ::: `:::.,::   ::::  :::`  ,,, ::`  .::  :::.::.  ,,, 
   ,::    ::.  ::: ::, ::`  ::: ::::::::.,::   ::::   :::::::` ::`   ::::::: :::::::. 
   ,::    ::.  ::: ::, ::`  :::  :::::::`,::    ::.    :::::`  ::`   ::::::   :::::.  
                                ::,  ,::                               ``             
                                ::::::::                                              
                                 ::::::                                               
                                  `,,`


https://www.thingiverse.com/thing:2537701
ANET A8 Spiral vase linear bushing by aeropic is licensed under the Creative Commons - Attribution - Non-Commercial license.
http://creativecommons.org/licenses/by-nc/3.0/

# Summary

Yet another linear bushing ?

Yes but this one is a bit special as, if you follow the process, it will print in "spiral vase" which means:
- it will be very accurate  !... The Spiral Vase setting of Slic3r will raise Z continuously avoiding a layer-change point which would cause a visible seam. The accuracy is given by parametrization of the diameters. It will fit direct from the printer once parametrized to your printer.
- A chamfer is included at both extremities on the inner and outer diameters. (no need to trim anything)
- it can be made springy
- it is self centering
- it is very light (around 1g each which means you win 50 g on the Y carriage)
- it has low friction and slides on the whole surface of the rods
- everything is customizable and MUST be customized (see below). As they cost nothing (around 2 cents each) you can play with them, print 4 or 5 prototypes to get the perfect fit. To open the customizer click on the button  "open in customizer"   just at the bottom right of the picture...

Only drawback, it must be installed inside a standard  bushing just because it has to be set inside a cylindrical housing to keep a regular shape.

They are installed on my Y axis and so far they do a great job!

see it here: https://youtu.be/BviIuek-uW4


you collect it, like it, made it ? please click on the like button and should you be on a good day, please consider leaving a $1 tip this would help for my R&D department ;-)

# Print Settings

Printer: ANET A8
Rafts: No
Supports: No
Resolution: 0.2 with a 0.4 nozzle
Infill: none - spiral vase

Notes: 
I printed in PLA. I don't use any lubricant.

This thing must be sliced with Slic3r using the spiral mode. See the 3rd picture. Do not forget to remove the bottom (with 0 layer).

EDIT : Cura slicer has also a spiralize mode. The settings are included in the last picture 
EDIT : if printing with Simplify3D you can find the vase mode within the layer section > Layer Settings > Single outline corkscrew printing mode (vase mode)...

Obviously, you shall print them one by one to get the spiral mode working...
Duration of print is only 5 minutes for one bushing.

Again, please read the next paragraph, the trimming must be done in customizer or (faster) directly with Openscad which is freeware.

# Custom Section

## let's customize it ...

It is mandatory to trim this model under the customizer or directly with openscad.

You must trim at least the following parameters :

// the outer diameter in mm
outerD=15.0;
Print some samples and adjust outerD first without modifying anything else. Once you get a bearing that fits exactly inside the bushing, you can play with the second parameter (inside diameter)

// inner diameter in mm
innerD=8.0;
The inner diameter can be set here. For a standard LM8UU, just leave this value to 8 mm

// this is used to trim the inner diameter (mm)
filament_margin = 0.92;
The spiral vase prints one perimeter just inside the perimeter of the rod... This "filament margin" is here to offset the inner diameter (increase this value to increase the size of the hole). On my printer with a noozle of 0.4 mm and a layer of 0.2, the filament width is around 0.45mm which means 0.90 on the diameter.
Basically start with 0.90 and play with this value to get the bushing nearly fully free on the rod (see the video to feel how accurate you have to be...)

You may as well play with the other parameters :

// height in mm
H=23.8; //23.8;
This is the height of the bushing. For a 24 mm, I left 0.2 mm free...

// number of spikes
N = 10;
If you want so, you can play with this to reduce or increase the number of blades or spikes.
10 seems to be the maximal value.

// spike angle
spike_angle = 30;
The blades are not perpendicular to the perimeter they are oriented with an angle. The bigger the angle, the more springy bushing you get. If you do not want any springy effect, set this value to 0.

// twist of blades in deg
blade_twist = 30;
On standard bushing (IGUS like) the spikes are fully radial which means that the friction is applied always on the same part of the rods. To get an even wear of the rods, you can twist the spikes pattern so that along the lenght of the bushing every part of the rods will be in contact of the printed bushing. Set it to 0 if you do not want this !

## my other ANET A8 mods

https://www.thingiverse.com/thing:2456797
https://www.thingiverse.com/thing:2430113
https://www.thingiverse.com/thing:2426747
https://www.thingiverse.com/thing:2494319
https://www.thingiverse.com/thing:2498478
https://www.thingiverse.com/thing:2502858
https://www.thingiverse.com/thing:2527328
https://www.thingiverse.com/thing:2640562

## EDIT : a picture after two months...

After two months in use I replaced the aluminium housings with those printed ones:
https://www.thingiverse.com/thing:2640562

This gave me the opportunity to perform a health check of the bushings. No surprize, as expected they behave very well ... On the picture you can see there are no sign of wear, only black oily spots showing that the friction is done here and there on each blade of the bushing.

That's cool to see they are in service qualified !

![Alt text](https://cdn.thingiverse.com/assets/1d/bd/37/eb/8f/20171112_105022.jpg)

## just for fun ;-)

incredible what i found this morning... I did not know this may exist !!!!!
Thank you to those who watch and like this little springy thing...

![Alt text](https://cdn.thingiverse.com/assets/82/df/c3/17/70/infinity.jpg)