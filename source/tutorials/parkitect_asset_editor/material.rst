Materials
=========

We've shipped some materials with the asset editor that you should use for your custom objects. These materials are special treated by the game. The materials are:

* Diffuse
* Specular
* CustomColorsDiffuse
* CustomColorsSpecular
* CustomColorsDiffuseTransparent
* CustomColorsSpecularTransparent
* CustomColorsDiffuseIllum
* CustomColorsSpecularIllum

As the name gives away there are two base materials: the Specular materials are used for metallic looking materials and the Diffuse ones for anything else. Then there are custom color variants that support having player-defined colors and the additional variants of those that support transparency and illuminated ones that [glow at night](Lights).

.. image:: image/material_diffuse_specular.png

These materials all have the same texture, the 256 palette, and are used by most objects in Parkitect. Because of that the GPU can use one texture for almost all objects. **We also can guarantee that if you use these materials your assets will keep rendering properly in future game updates. If you roll your own materials they may (and probably will) stop working in the future and you have to update your asset pack. That's why we strongly encourage you to use our materials.**

Using the materials
-------------------

As you can see the 256 palette is a very simple texture with 256 colors and the largest part of Parkitect is build on these colors. To use them on your models you need to import the 256 palette texture in your 3d modeling program. The texture is shipped with the asset editor and is located at `Assets/Resources/Textures/256palette.tga`. The next step is to map the texture on your model, also called UV mapping.

> Tutorials on how to map uv's with your favorite 3d program can be easily found on the internet.

Next, map every face of the model to a color on the texture. The outlines of the face don't have to follow the outlines of a color. As long as every vertex is inside the square it will work correctly.

Make sure the material name of your model matches with one of our models. Otherwise it will not be replaced properly in-game, leading to broken models in the future. Use `Diffuse` or `Specular` for non recolorable objects and `CustomColorsDiffuse` or `CustomColorsSpecular` for recolorable objects.

Export the model as fbx, obj or another format that Unity can read and copy it to `Assets/Resources` in your asset project. Select the model and make sure the that "Material naming" has the value of "From model's material" in the inspector.

.. image:: image/material_naming.png

> For some model formats you need to check the scale factor of the model in the inspector. For example, fbx needs a factor of 100 to match 1 unit with 1 tile in Parkitect.

.. _material_custom_colors:

Custom coloring
---------------
In the bottom right of the 256 palette you see 4 special colors. Those are the colors that can be recolored in-game. The pixels are in the following order:

+--------+----------+
| Color  | Target   |
+--------+----------+
| Indigo | Color 4  |
+--------+----------+
| Blue   | Color 3  |
+--------+----------+
| Green  | Color 2  |
+--------+----------+
| Red    | Color 1  |
+--------+----------+

.. image:: image/256pallet.png

Your object can support a maximum of 4 custom colors. Map the faces of the objects that needs to be recolored to these 4 special colors. Don't skip a color with mapping. For example never use color 1, 3 and 4 but instead use color 1, 2 and 3.

When you've mapped the colors you also need to [enable recoloring](Custom-colors) on your object and set some default colors.

