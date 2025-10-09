# pBird-Edge
Custom FDP focused training edge for climbers. This device is intended to be an ergonomic egde, that focuses on training the FDP tendon(s). Tendon isolation is acheived by enforcing certain joint angles when lifting, when the intended form is lost or can no longer be held, the rollers force the user to drop the device (heavy inspiration from NS Climber Mobeta and his Hand of God training device). The joint angles are enforced by the geometry of the device.  

![alt text](https://github.com/dn757657/pBird-Edge/blob/main/media/pBird1.jpg?raw=true)

# Basics
There does not appear to be explicit agreement concerning joint angles in the small academic survey conducted to make these models/devices. Based on my interpretation of the works cited below, a good starting point for FDP isolation is: Wrist 0, MCP 15, PIP 55, DIP 55 joint angles in degrees.

Works Cited:
- DOI: 10.1371/journal.pone.0160301
- DOI: 10.1016/j.jbiomech.2005.08.027
- DOI: 10.1109/IEMBS.2009.5333525
- DOI: https://doi.org/10.1186/1749-799X-3-27

# Materials Required
- 3D printer access or access to a 3D printing service
- CAD (ideally solidworks)
- Zip Ties (1.3 x 5mm ish cross section measurements, can be adjusted in model)
- super glue (optional)
- 3mm diam. x 10mm length metal dowel pins (Mcmaster Carr)
- hammer, side cutters, basic hand tools

# Measuring
Custom fitment is essential to prevent overloading a single finger, and minimize chance of injury. Below is the suggested measurement methodology:
- Mark the apex atop each join as best as possible
  - bending the knuckle can help estimate the joint center/ axis of rotation
  - note that the skin here moves significantly on top of the knuckle, so marking while flexed yeilds poor results
- measure the width of each finger (planar with nail)
  - add an additional 10mm or ~60% to the pinky width to make it comfy to roll over naturally when pulling, this is why its wide
  - add an additional 5mm or 25% to the index width for the same reason
  - not verified on a large dataset, experience may vary
- measure the depth of each finger (perpendicular to nail)
  - best results here if you measure the finger while compressed, as this is the state assumed when using the device
- photograph each marked hand, ensure the scene contains an object of known size for later scaling
- import these photos into a CAD software of your choice
- measure the distance between each joint along the axis of the finger
  - in my experience results are better when the segment from DIP joint to finger end is measured with the end of the finger compressed
- measuring knuckle offsets, as they are defined in the models is slightly trickier, best results thus far are as follows, there are 3 offset for each knuckle
- first draw a line in the CAD where the photos are imported, perpendicular to the line along the middle finger used to measure the middle finger joint distances (denoted Line A)
  - the intersection of this perpendicular line and the line following the middle finger is denoted intersection A
- draw a line parallel to that line, that also passes through the intersection of the line along each other finger, and the MCP apex (denoted intersection B), this creates a new intersection with the above drawn line (denoted intersection C)
- the distance from intersection B to intersection C is one offset, the distance along line A from intersection C to intersection A is anmother
  - where to enter these is hopefulyl more clear in the model
- the final offset is the height offset, as if the hand is on a table, some knuckles are taller than others.
  - best results have been using a depth gauge, each offset here is measured relative to the middle knuckle
  - my best results have been dividing the values obtained here by 2

This is all the measurements required for making a custom pBird Device.

# CAD
For now models are only available as solidworks models, I am not aware of methods for converting to open source models and maintaining the parametric relationships within the assembly for custom finger layouts, but reach out if you have a solution to make models available in other softwares (or just do it). The models have not been trialed with many different hands, despite doing my best to make them parametric and adaptable, some tweaking may be required. Please post an issue/PR if you have fixes or improvements.

Some basics about the model:
- each finger is a subassmbly conatining some master geometry (pBird_master) that is shared among fingers
  - this makes adjusting these shared features easy as theyre all shared, changing one means changing them all
  - some exmaples being ledge size, roller offsets, etc
- each finger base has a finger sketch, most of the finger measurements go here
- i = index, r = ring, m = middle, p = pinky
- parts with "ext" in the part name are to flesh out the bases, and may be janky
  - more on this later

Usage:
- edit each finger sketch for your finger measurements
  - optional: if you interpret the cited works differently, or what to try a mix of FDP/FDS, changes the joint angles!
    - make sure the joint angles match for each finger in this instance
- edit the knuckle offsets in the 3D sketches labelled "knuckle placement"
- optional: edit the finger seperation angles
  - currently no convenient way to do this other than going into the mates of the finger subassembly and modifying the angle constraint
  - these are finger splay angles relative to the middle finger, the angles in the model provided are what I find comfy

Critical Fits:
- the 3mm pin interface with the rollers (roller axis hole) should be a serious interference fit
  - print a test peice to check fits, as each printer is different
- the 3mm pin interface with the plates (roller axis holes) should be loose, its essential for the rollers to roll freely
- zip tie holes
  - make sure your zip ties are snug, and should be difficult to get through each part, better fit results in a more precise device
- it is recommended to test fit these items using test prints to dial in these feature sizes

# Printing
- export all files to STL
  - parts with "ext" in the part name should be exported with parts marked "base" for each finger, theyre meant to be a single part
  - saving them as a single STL will merge them
- print however
  - prototypes shown use ABS filament, no supports, 0.1mm layers

# Assembly
- clean up parts
- press pins into either end of each roller, leaving enough pin exposed to interface with the adjacent plates
- ensure rollers roll freely in the plates
  - if not ream plate holes until they do
- force zip ties through each part in the correct order
- install rollers
- compress device for final assembly using the heads of other zip ties
  - pull as tight as possible
  - optional: glue between bases and plates for permanent/ stronger fixture

Complete
