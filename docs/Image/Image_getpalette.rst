==========================
Image getpalette
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getpalette

----

Getpalette
----------------------------

| Use the ``Image.getpalette(rawmode='RGB')`` method to return the image palette as a list of color values [r, g, b, …], or None if the image has no palette.
| rawmode - The mode in which to return the palette. None will return the palette in its current mode.

| The code below converts an image to have a palette then gets the palette for printing.

.. code-block:: python

    from PIL import Image

    with Image.open("test_images/shapes.png") as im:
        im1 = im.convert(mode="P", palette=Image.Palette.ADAPTIVE)
        print(im1.getpalette())
        # [0, 0, 0, 205, 85, 207,...]
            



