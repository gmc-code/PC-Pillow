==========================
ImageFilter Find Edges
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Find Edges
-----------

| Use the ``Image.filter(ImageFilter.FIND_EDGES)`` method to find the edges of parts of the image.
| Best results require an image in RGB mode rather than RGBA.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        im_rgb = im.convert(mode='RGB')
        new_im = im_rgb.filter(ImageFilter.FIND_EDGES)
        new_im.save("filters/find_edges.png")


.. image:: images/compare_find_edges.png
    :scale: 50%
    :align: center
    