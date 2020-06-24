# TV

TV's are path attachments that are on the side of paths/queues.

## Color settings

Every object support custom colors. Check [this](Custom-colors) page for more info on custom color settings.

## TV settings

**Screen object**: the child game object of the TV that should show the image. Parkitect will replace the material on this object with the screen material.

## Setup screen object

Your TV object should consist of two models. The pole with a TV encasing and a child glass panel model, see the image below.

![tv](https://i.imgur.com/EECsg4Q.png)

The pole with TV case can be modeled and mapped normally following the [custom colors](custom-colors) guide. The screen 
requires 1 material named `TVImage`. If you name the material correctly, the game will replace the material with the real TV shader that shows images of your park. 

Make sure you've dragged the child screen game object to the `Screen object` setting of the TV settings.

![screen object](https://i.imgur.com/uRut3L2.png)
