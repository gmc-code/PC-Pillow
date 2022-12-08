==========================
Image getextrema
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getextrema

----

Getextrema
----------------------------

| Use the ``Image.getextrema()`` method to return the minimum and maximum pixel values for each band in the image.
| For a single-band image, it returns a 2-tuple containing the minimum and maximum pixel value. 
| For a multi-band image, it returns a tuple containing one 2-tuple for each band.


.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getextrema())
        # ((255, 255), (127, 255), (39, 255), (0, 255))



