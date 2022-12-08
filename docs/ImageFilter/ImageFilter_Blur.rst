==========================
ImageFilter Blur
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Blur
----------------------

| Use the ``Image.filter(ImageFilter.BLUR)`` method to blur an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.BLUR)
        new_im.save("filters/blur.png")


.. image:: images/compare_blur.png
    :scale: 50%
    :align: center


