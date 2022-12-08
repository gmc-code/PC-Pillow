==========================
ImageOps flip
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageOps.html#PIL.ImageOps.flip

----

Flip
---------------------------

| Use the ``ImageOps.flip(image)`` method to return an image that has been flipped vertically (top to bottom).

.. code-block:: python

    from PIL import Image, ImageOps

    with Image.open("test_images/shapes.png") as im:
        im1 = ImageOps.flip(im)
        im1.save("imageOps/flip.png")



.. image:: images/compare_flip.png
    :scale: 50%
    :align: center

