==========================
ImageOps mirror
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.mirror

----

Mirror
---------------------------

| Use the ``ImageOps.mirror(image)`` method to return an image that has been flipped horizontally (left to right).

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/shapes.png") as im:
        im1 = ImageOps.mirror(im)
        im1.save("imageOps/mirror.png")



.. image:: images/compare_mirror.png
    :scale: 50%
    :align: center

