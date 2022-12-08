==========================
ImageFilter GaussianBlur
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.GaussianBlur

----


GaussianBlur
----------------------

| Use the ``Image.filter(ImageFilter.GaussianBlur(radius))`` method to blur an image.
| Blurs the image with a sequence of extended box filters, which approximates a Gaussian kernel. 

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.GaussianBlur(1))
        new_im.save("filters/GaussianBlur1.png")
        new_im = im.filter(ImageFilter.GaussianBlur(2))
        new_im.save("filters/GaussianBlur2.png")


.. image:: images/compare_GaussianBlur.png
    :scale: 50%
    :align: center      

