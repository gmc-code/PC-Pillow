==========================
ImageOps colorize
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.colorize

----

Colorize
---------------------------


| Use the ``ImageOps.colorize(image, black, white, mid=None, blackpoint=0, whitepoint=255, midpoint=127)`` method to colorize a grayscale image. 
| The black and white arguments should be RGB tuples; this function calculates a color wedge mapping all black pixels in the source image to the first color, and all white pixels to the second color.

.. py:function:: ImageOps.colorize(image, black, white, mid=None, blackpoint=0, whitepoint=255, midpoint=127)

    | **image** - The image to colorize.
    | **black** - The color to use for black input pixels.
    | **white** - The color to use for white input pixels.
    | **mid** - The color to use for midtone input pixels.
    | **blackpoint** - an int value [0, 255] for the black mapping.
    | **whitepoint** - an int value [0, 255] for the white mapping.
    | **midpoint** - an int value [0, 255] for the midtone mapping.

| The code below colorizes an image.
| The image is converted to greyscale first.

.. code-block:: python

    from PIL import Image, ImageOps

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/cliffs.jpg") as im:
        im1 = ImageOps.grayscale(im)
        im1 = ImageOps.colorize(im1, (135,62,35), "white")
        im1.save("imageOps/colorize.png")


.. image:: images/compare_colorize.png
    :scale: 50%
    :align: center

