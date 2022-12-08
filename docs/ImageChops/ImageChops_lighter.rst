==========================
ImageChops lighter
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.lighter

----

Lighter
---------------------------

| Use the ``ImageChops.lighter(image1, image2)`` method to compare the two images, pixel by pixel, and returns a new image containing the lighter values.
| out = max(image1, image2)

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.lighter(im1, im2)
            im_out.save("chops/lighter.png")


.. image:: images/compare_lighter.png
    :scale: 50%
    :align: center


