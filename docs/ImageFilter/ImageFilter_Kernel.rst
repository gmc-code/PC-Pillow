==========================
ImageFilter Kernel
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.Kernel

----

Kernel
----------------------

| Use the ``Image.filter(ImageFilter.Kernel(size, kernel, scale=None, offset=0)`` method to apply a convolution to an image.

.. py:function:: ImageFilter.Kernel(size, kernel, scale=None, offset=0)

    | Parameters:
    | size - Kernel size, given as (width, height). This must be (3, 3) or (5, 5).
    | kernel - A sequence containing kernel weights (integer or floating point). 
    | e.g. (-1, -1, -1, -1, 9, -1, -1, -1, -1)
    | scale - Scale factor. If given, the result for each pixel is divided by this value. The default is the sum of the kernel weights.
    | offset - Offset. If given, this value is added to the result, after it has been divided by the scale factor.

Returns type: An image.

.. code-block:: python

    from PIL import Image, ImageFilter

   
    with Image.open("test_images/river_valley.jpg") as im:
        new_im = im.filter(ImageFilter.Kernel((3, 3), (-1, -1, -1, -1, 9, -1, -1, -1, -1), 1, 0))
        new_im.save("filters/Kernel.png")

        new_im = im.filter(ImageFilter.Kernel((3, 3), (0, -1, 0, -1, 5, -1, 0, -1, 0), 1, 0))
        new_im.save("filters/Kernel2.png")


.. image:: images/compare_Kernel.png
    :scale: 50%
    :align: center


