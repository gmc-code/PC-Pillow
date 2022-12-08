==========================
ImageChops invert
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.invert

----

Invert
---------------------------

| Use the ``ImageChops.invert(image)`` method to invert an image.
| out = MAX - image

.. py:function:: ImageChops.invert(image)

    | returns an inverted image
    | **image** is the image to invert.

| The code below inverts an image.
| The original png is in RGBA mode so when inverted unexpected results are seen.
| After converting to RGB mode, the colours are inverted as expected.

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/circles.png") as im:
        im_inv = ImageChops.invert(im)
        im_inv.save("chops/invert.png")


.. image:: images/compare_invert.png
    :scale: 50%
    :align: center

