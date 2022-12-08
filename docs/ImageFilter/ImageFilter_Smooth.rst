==========================
ImageFilter Smooth
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Smooth
----------------------

| Use the ``Image.filter(ImageFilter.SMOOTH)`` method to smooth an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.SMOOTH)
        new_im.save("filters/smooth.png")

| Unfiltered, smooth and smooth more are compared below:

.. image:: images/compare_smooth_more.png
    :scale: 50%
    :align: center
        
  