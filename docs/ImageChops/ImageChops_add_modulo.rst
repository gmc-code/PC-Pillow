==========================
ImageChops add_modulo
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.add_modulo

----

Add modulo
---------------------------

| Use the ``ImageChops.add_modulo(image1, image2)`` method to add two images, without clipping the result.
| out = ((image1 + image2) % MAX)

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.add_modulo(im1, im2)
            im_out.save("chops/add_modulo.png")


.. image:: images/compare_add_modulo.png
    :scale: 50%
    :align: center

