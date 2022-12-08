==========================
ImageFilter Contour
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#filters

----

Contour
----------------------

| Use the ``Image.filter(ImageFilter.CONTOUR)``method to contour an image.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.CONTOUR)
        new_im.save("filters/contour.png")


.. image:: images/compare_contour.png
    :scale: 50%
    :align: center
         