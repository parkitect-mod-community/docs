Deco
====

Deco objects are static objects that serve no other purpose than for decoration. For example trees, vases and other plants or deco objects.

Color settings
--------------

Every object support custom colors. Check :ref:`custom colors <custom_color>` page for more info on custom color settings.

Placement settings
------------------

**Build on grid**: whether this object can only be built on the grid (on) or can be placed freely (off).

**Snaps to center**: whether this objects is snapped to the center of a tile (on) or the corner (off) by default.

**Grid subdivision**: by default the placement grid of an object is the same size as 1 tile. This setting can make the placement grid smaller than a tile. A value of 3 will create a 3x3 grid within 1 tile.

**Height delta**: the step size when the player raises/lowers the object. Most objects included with the game use a value of 0.25, so to make sure everything fits nicely together your custom objects should only change this if there's a good reason for it.

Size Settings
-------------

**Is resizable**: whether this object is resizable.

If `Is resizable` is enabled, players can resize the object in the game. The object will always have a size of 1 by default which is the same size as shown in the asset editor.

**Min size**: Any value _lower_ than 1 will mean that the player can make the object smaller by a maximum of this value. For example: a value of 0.2 means the player can make the object 5 times smaller.

**Max size**: Any value _higher_ than 1 will mean that the player can make the object larger by a maximum of this value. For example: a value of 7 means the player can make the object 7 times larger.

Visibility Settings
-------------------

**Can see through**: whether guests can "see through" this object (on) or whether it blocks the view (off). Should be on for most objects, especially small props or details. Only walls or bigger deco objects that roughly fill an entire tile should disable this to block the view.

**Blocks rain**: whether guests are protected from rain while they are under this object (on) or not (off). Should be disabled for most objects. Only roofs or objects that fulfill a similar purpose (e.g. pavillions) should enable this.
