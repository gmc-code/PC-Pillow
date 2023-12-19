==========================
Image getbands
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getbands

----

Getbands
----------------------------

| Use the ``Image.getbands()`` method to return a tuple containing the name of each band in the image. For example, getbands on an RGB image returns ('R', 'G', 'B').

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getbands())
        # ('R', 'G', 'B', 'A')

