==========================
Image getbbox
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getbbox

----

Getbbox
----------------------------

| Use the ``Image.getbbox()`` method to return the bounding box of the non-zero regions in the image.
| The bounding box is returned as a 4-tuple defining the left, upper, right, and lower pixel coordinate.
| If the image is completely empty, this method returns None.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getbbox())
        # (26, 26, 230, 230)



