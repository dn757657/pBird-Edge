# pBird-Edge
Custom FDP focused training edge for climbers. This device is intended to be an ergonomic egde, that focuses on training the FDP tendon(s). Tendon isolation is acheived by enforcing certain joint angles when lifting, when the intended form is lost or can no longer be held, the rollers force the user to drop the device (heavy inspiration from NS Climber Mobeta and his Hand of God training device). The joint angles are enforced by the geometry of the device.  

# Basics
There does not appear to be explicit agreement concerning joint angles in the small academic survey conducted to make these models/devices. Based on my interpretation of the works cited below, a good starting point for FDP isolation is: Wrist 0, MCP 15, PIP 55, DIP 55 joint angles in degrees.

Works Cited:
- DOI: 10.1371/journal.pone.0160301
- DOI: 10.1016/j.jbiomech.2005.08.027
- DOI: 10.1109/IEMBS.2009.5333525
- DOI: https://doi.org/10.1186/1749-799X-3-27

# Measuring
Custom fitment is essential to prevent overloading a single finger, and minimize chance of injury. Below is the suggested measurement methodology:
- Mark the apex atop each join as best as possible
  - bending the knuckle can help estimate the joint center/ axis of rotation
  - note that the skin here moves significantly on top of the knuckle, so marking while flexed yeilds poor results
- measure the width of each finger (planar with nail)
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
