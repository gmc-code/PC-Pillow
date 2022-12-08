==========================
ImageChops constant
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.constant

----

Constant
---------------------------

| Use the ``ImageChops.constant(image, value)`` to return an image with a given grey level.

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("shapes/x.png") as im1:
        im_out = ImageChops.constant(im1, 205)
        im_out.save("chops/constant.png")



.. image:: images/constant.png
    :scale: 50%
    :align: center


