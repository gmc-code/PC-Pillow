==========================
ImageFilter Detail
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Detail
----------------------

| Use the ``Image.filter(ImageFilter.DETAIL)`` method to detail an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.DETAIL)
        new_im.save("filters/detail.png")


.. image:: images/compare_detail.png
    :scale: 50%
    :align: center
        
