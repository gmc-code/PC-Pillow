==========================
ImageChops subtract
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.subtract

----

Subtract
---------------------------

| Use the ``ImageChops.subtract(image1, image2, scale=1.0, offset=0)`` method subtracts two images, dividing the result by scale and adding the offset. 
| If omitted, scale defaults to 1.0, and offset to 0.0.
| out = ((image1 - image2) / scale + offset)

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.subtract(im1, im2, scale=1.0, offset=0)
            im_out.save("chops/subtract.png")

.. image:: images/compare_subtract.png
    :scale: 50%
    :align: center

