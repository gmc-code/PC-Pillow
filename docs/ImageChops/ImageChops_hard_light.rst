==========================
ImageChops hard_light
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.difference

----

Hard_light
---------------------------

| Use the ``ImageChops.hard_light(image1, image2)`` method to return an image that superimposes two images on top of each other using the Hard Light algorithm.


.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.hard_light(im1, im2)
            im_out.save("chops/hard_light.png")


.. image:: images/compare_hard_light.png
    :scale: 50%
    :align: center
