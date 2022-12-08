==========================
ImageFilter Emboss
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Emboss
----------------------

| Use the ``Image.filter(ImageFilter.EMBOSS)`` method to emboss an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.EMBOSS)
        new_im.save("filters/emboss.png")


.. image:: images/compare_emboss.png
    :scale: 50%
    :align: center
         