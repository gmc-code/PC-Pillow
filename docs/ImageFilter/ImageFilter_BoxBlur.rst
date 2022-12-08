==========================
ImageFilter BoxBlur
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.BoxBlur

----

BoxBlur
----------------------

| Use the ``Image.filter(ImageFilter.BoxBlur(radius))`` method to blur an image.
| Blurs the image by setting each pixel to the average value of the pixels in a square box extending radius pixels in each direction.

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.BoxBlur(1))
        new_im.save("filters/BoxBlur.png")
        new_im = im.filter(ImageFilter.BoxBlur(2))
        new_im.save("filters/BoxBlur.png")


.. image:: images/compare_BoxBlur.png
    :scale: 50%
    :align: center      

