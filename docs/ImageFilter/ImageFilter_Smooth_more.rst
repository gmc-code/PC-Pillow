==========================
ImageFilter Smooth More
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Smooth more
----------------------

| Use the ``Image.filter(ImageFilter.SMOOTH_MORE)`` method to smooth more an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.SMOOTH_MORE)
        new_im.save("filters/smooth_more.png")

| Unfiltered, smooth and smooth more are compared below:

.. image:: images/compare_smooth_more.png
    :scale: 50%
    :align: center
        
  