==========================
Image getpixel
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getpixel

----

Getpixel
----------------------------

| Use the ``Image.getpixel(xy)`` method to the pixel value at a given position given as (x, y). 
| If the image is a multi-layer image, this method returns a tuple.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getpixel((32, 32)))
        # (255, 127, 39, 255)



