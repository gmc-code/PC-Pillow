==========================
ImageOps scale
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.scale

----

Scale
---------------------------

| Use the ``ImageOps.scale(image, factor, resample=Resampling.BICUBIC)`` method to return an image that has been scaled by a specific factor.
| **factor** - A factor greater than 1 expands the image, between 0 and 1 contracts the image.


.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/shapes.png") as im:
        im1 = ImageOps.scale(im, 1.25)
        im1.save("imageOps/scale.png")



.. image:: images/compare_scale.png
    :scale: 50%
    :align: center

