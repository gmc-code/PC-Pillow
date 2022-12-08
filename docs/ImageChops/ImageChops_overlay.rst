==========================
ImageChops overlay
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.overlay

----

Overlay
---------------------------

| Use the ``ImageChops.overlay(image1, image2)`` method to overlay 2 images of the same size.

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.overlay(im1, im2)
            im_out.save("chops/overlay.png")


.. image:: images/compare_overlay.png
    :scale: 50%
    :align: center

