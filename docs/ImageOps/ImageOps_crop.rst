==========================
ImageOps crop
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.crop

----

Crop
---------------------------

| Use the ``ImageOps.crop(image, border=0)`` method to remove a border from an image. The same amount of pixels are removed from all four sides. This function works on all image modes.
| **border** - The number of pixels to remove.

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/shapes.png") as im:
        im1 = ImageOps.crop(im, border=32)
        im1.save("imageOps/crop.png")



.. image:: images/compare_crop.png
    :scale: 50%
    :align: center

