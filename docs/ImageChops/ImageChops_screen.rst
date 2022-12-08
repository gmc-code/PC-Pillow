==========================
ImageChops screen
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.screen

----

Screen
---------------------------

| Use the ``ImageChops.screen(image1, image2)`` method superimpose two inverted images on top of each other.
| out = MAX - ((MAX - image1) * (MAX - image2) / MAX)

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.screen(im1, im2)
            im_out.save("chops/screen.png")


.. image:: images/compare_screen.png
    :scale: 50%
    :align: center

