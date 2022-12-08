==========================
ImageChops soft_light
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.soft_light

----

Soft_light
---------------------------

| Use the ``ImageChops.soft_light(image1, image2)`` method superimposes two images on top of each other using the Soft Light algorithm.

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.soft_light(im1, im2)
            im_out.save("chops/soft_light.png")


.. image:: images/compare_soft_light.png
    :scale: 50%
    :align: center

