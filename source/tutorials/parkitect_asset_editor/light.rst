Light
=====

Lights look nice, especially during night. You can put lights onto any object, but usually you'll use them on [Lamps](Lamp) or [Deco](deco).
There are two types of light effects you can use.

By default lights are always on, even during the day. For lights that should be on during the night and off during the day there are the following settings:

**Turn on at night**: whether this light only turns on during the night (on) or is always on (off).

If your object uses [custom colors](custom-colors) these additional settings are available for actual lights (doesn't matter for glow effects since they use the custom colors from the material):

**Use custom colors**: whether the emitted light should be tinted using one of the custom colors (on) or not (off).

**Custom color slot**: pick which of the custom color slots should be used for tinting the emitted light

Glow Effect
~~~~~~~~~~~

You can give parts of your object a glow:

.. image:: image/glow_effect.png

This is achieved by using the [CustomColorsDiffuseIllum/CustomColorsSpecularIllum material](Materials) on the parts of your object that should glow.
This effect has **no performance costs**, so you can use it as much as you want.

Actual Light Effect
~~~~~~~~~~~~~~~~~~~

.. image:: image/light_effect.png

This effect **has performance costs**, so consider if your object actually needs this before using it, especially for small objects that players tend to spam all over the park. For example, for small light bulbs (such as the ones we got on the rides or string lights) it is enough to give them a glow effect, they don't actually have to light up the surroundings.
Ideally also don't use more than one light source per object. If your object has multiple visible light sources you can probably approximate them with a single light component.

To use an actual light, add an empty GameObject to your custom object and position it where the light should originate from, then add a Light component to it.

.. image:: image/light_lamp.png

The light type can either be "Point" or "Spot". Leave **shadows disabled** as that can have massive performance costs.
Some good default values are:

For point lights
----------------
* Range: 4
* Intensity: 2

For spot lights
---------------
* Range: 1.5
* Spot angle: 100
* Intensity: 2.5


You can also combine both effects of course:

.. image:: image/light_combined.png
