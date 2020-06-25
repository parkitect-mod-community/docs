Train
=====

Custom trains for most of the tracked rides in the game.
The Resources/Reference Objects/Tracks folder contains reference track segments for most coaster types that you can use for scale reference, especially for determining where the car wheels should go.
Note that the collision bounds, tunnel sizes and slope/curve radius of tracked rides depend on the ride type, not on the type of trains used by that ride, so generally it would be a good idea to keep your custom trains roughly within the same dimensions as the default trains used by that ride (otherwise your trains could clip through collision bounds/tunnels etc.).

Color Settings
--------------

Check [this](Custom-colors) page for more info on custom color settings.

Car Model
---------


You can use a different car model for the front of the train than for the remaining cars.

The pivot of your car should be centered between the front wheels and vertically aligned with the spot where the wheels will touch the surface of the track:

.. image:: image/ride_pivot.png

There needs to be an empty transform named "backAxis", positioned in the same way as the cars pivot but in the location of the back wheels:

.. image:: image/ride_back_axis.png

To make the wheels steer in curves split them into a separate part named "WheelsFront" or "WheelsBack" respectively.
The wheels are not very clearly visible on some types of coasters or the curve radius of the track might be so wide that it's not really noticeable whether the wheels are steering or not. In this case you shouldn't split the wheels into a separate part.

.. image:: image/ride_wheel.png

Car Settings
------------

**Seat waypoint offset**: defines a point that is offset by the given distance from the seat locations of the train. It is shown as a red sphere in the asset preview. Guests will walk up to this spot when entering the car, so you should move this to a spot where they won't clip through the car model too badly when entering.

.. image:: image/train_seat_waypoint.png

**Offset front**/**Offset back**: a distance relative to the pivot/backAxis marker of the car to determine where the car ends, used for collision detection with other trains and to determine where to position the next car in the train. Shown as white lines with a "Front"/"Back" label in the preview. Move them roughly to the ends of the car model.

.. image:: image/waypoint_offset_back.png



Seats
-----

It's probably easiest to create seat markers in your modeling tool - simply create empty transforms named "Seat". Alternatively you can also add them in Unity.

Restraints
----------

The restraints need to be opened by default in your car model and split into a separate part. The restraint pivots needs to be placed such that the restraint can rotate around its local X-Axis.
Configure the angle at which the closed restraint should be positioned by adjusting the **Closed angle** property. You'll see a preview of all affected restraints to assist you with determining the correct value for this property.

.. image:: image/train_restraint.png


Path Finding
------------
