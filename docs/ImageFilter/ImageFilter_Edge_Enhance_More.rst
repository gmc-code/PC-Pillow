================================
ImageFilter Edge Enhance More
================================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Edge enhance more
----------------------

| Use the ``Image.filter(ImageFilter.EDGE_ENHANCE_MORE)`` method to edge enhance more an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.EDGE_ENHANCE_MORE)
        new_im.save("filters/edge_enhance_more.png")


| Unfiltered, edge_enhance and edge_enhance_more are compared below:

.. image:: images/compare_edge_enhance_more.png
    :scale: 50%
    :align: center
