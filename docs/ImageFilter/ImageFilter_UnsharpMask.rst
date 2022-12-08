==========================
ImageFilter UnsharpMask
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.UnsharpMask

----

UnsharpMask
----------------------

| Use the ``Image.filter(ImageFilter.UnsharpMask(radius=2, percent=150, threshold=3))`` method to sharpen an image.
| **radius** - Blur Radius
| **percent** - Unsharp strength, in percent
| **threshold** - Threshold controls the minimum brightness change that will be sharpened

.. code-block:: python

    from PIL import Image, ImageFilter

    with Image.open("test_images/alph_blocks.png") as im:
        new_im = im.filter(ImageFilter.UnsharpMask(radius=1, percent=200, threshold=3))
        new_im.save("filters/UnsharpMask1.png")
        new_im = im.filter(ImageFilter.UnsharpMask(radius=2, percent=150, threshold=3))
        new_im.save("filters/UnsharpMask2.png")

.. image:: images/compare_UnsharpMask.png
    :scale: 50%
    :align: center

.. image:: images/compare_UnsharpMask2.png
    :scale: 50%
    :align: center
