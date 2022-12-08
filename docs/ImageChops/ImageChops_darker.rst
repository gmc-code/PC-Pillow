==========================
ImageChops darker
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.darker

----

Darker
---------------------------

| Use the ``ImageChops.darker(image1, image2)`` to compare the two images, pixel by pixel, and returns a new image containing the darker values.
| out = min(image1, image2)

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.darker(im1, im2)
            im_out.save("chops/darker.png")



.. image:: images/compare_darker.png
    :scale: 50%
    :align: center


