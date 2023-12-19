==========================
Image getcolors
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getcolors

----

Getcolors
----------------------------

| Use the ``Image.getcolors(maxcolors=256)`` method to return an unsorted list of (count, pixel) values used in the image.
| The colors will be in the image's mode. For example, an RGB image will return a tuple of (red, green, blue) color values, and a P image will return the index of the color in the palette.
| maxcolors - Maximum number of colors. If this number is exceeded, this method returns None.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getcolors())
        # [(52144, (255, 255, 255, 0)), (13392, (255, 127, 39, 255))]





