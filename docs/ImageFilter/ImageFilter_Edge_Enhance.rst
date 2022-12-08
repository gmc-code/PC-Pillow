==========================
ImageFilter Edge Enhance
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Edge enhance
----------------------

| Use the ``Image.filter(ImageFilter.EDGE_ENHANCE)`` method to edge enhance an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.EDGE_ENHANCE)
        new_im.save("filters/edge_enhance.png")

| Unfiltered, edge_enhance and edge_enhance_more are compared below:

.. image:: images/compare_edge_enhance_more.png
    :scale: 50%
    :align: center
