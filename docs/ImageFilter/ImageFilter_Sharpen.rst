==========================
ImageFilter Sharpen
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Sharpen
----------------------

| Use the ``Image.filter(ImageFilter.SHARPEN)`` method to sharpen an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.SHARPEN)
        new_im.save("filters/sharpen.png")


.. image:: images/compare_sharpen.png
    :scale: 50%
    :align: center
