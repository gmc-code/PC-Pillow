==========================
Image getprojection
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getprojection

----

Getprojection
----------------------------

| Use the ``Image.getprojection()`` method to return two sequences, indicating where there are non-zero pixels (with a 1) along the X-axis and the Y-axis, respectively.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.getprojection())
        # ([1, 1, 1,....], [1, 1, 1,  ...])



