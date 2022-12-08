==========================
ImageOps invert
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.invert

----

Invert
---------------------------

| Use the ``ImageOps.invert(image)`` method to invert an image.
| Only L and RGB images can be used.

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/cliffs.jpg") as im:
        im1 = ImageOps.invert(im)
        im1.save("imageOps/invert.png")



.. image:: images/compare_invert.png
    :scale: 50%
    :align: center

