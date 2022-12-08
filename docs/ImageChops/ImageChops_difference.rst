==========================
ImageChops difference
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.difference

----

Difference
---------------------------

| Use the ``ImageChops.difference(image1, image2)`` method to return the absolute value of the pixel-by-pixel difference between the two images.
| out = abs(image1 - image2)

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.difference(im1, im2)
            im_out.save("chops/difference.png")


.. image:: images/compare_difference.png
    :scale: 50%
    :align: center
