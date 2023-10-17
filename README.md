# Pinsert

Many times, when designing parts for 3D printing, the part will be physically larger than the build volume of the 3D printer. 
One option for dealing with this is to split the part into multiple smaller pieces, each of which will fit into the build volume of the printer. 
These pieces can later be assembled into the full part. The use of alignment pins eases assembly of these separate pieces.

Pinsert is a FreeCAD macro that can be used to quickly create holes for these alignment pins withing a given model.

The user can create sketches on the splitting planes of the model. These sketches contain lines whose endpoints can be selected to tell the
macro where to insert a cylinder that will define the alignment pin hole(s). The user will define the diameter and length of the pin hole at the
time of macro execution. The macro inserts a cylinder whose centroid is attached to each selected sketch point. This way, if the user needs to
modify the design, and the alignment pin location sketches change, the alignment pin holes will move with those sketches.

Prior to splitting the model, a Boolean Subtract operation should be performed to create the holes. The cylinder bodies that were created by the macro
will be subtracted from the base body of the part.

INSTALLATION:

Copy the file Pinsert.FCMacro into the Macros folder of your choice.
