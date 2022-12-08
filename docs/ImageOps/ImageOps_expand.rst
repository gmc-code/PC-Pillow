==========================
ImageOps expand
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.expand

----

Expand
---------------------------

| Use the ``ImageOps.expand(image, border=0, fill=0)`` method to return an image that has a border added to it.
| **border** - Border width, in pixels.
| **fill** - Pixel fill value (a color value). Default is 0 (black).

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/shapes.png") as im:
        im1 = ImageOps.expand(im, border=25, fill="red")
        im1.save("imageOps/expand.png")



.. image:: images/compare_expand.png
    :scale: 50%
    :align: center

