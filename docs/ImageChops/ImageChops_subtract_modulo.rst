=============================
ImageChops subtract_modulo
=============================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.subtract_modulo

----

Subtract_modulo
---------------------------

| Use the ``ImageChops.subtract_modulo(image1, image2)`` method subtracts two images, dividing the result by scale and adding the offset. 
| If omitted, scale defaults to 1.0, and offset to 0.0.
| out = ((image1 - image2) / scale + offset)

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.subtract_modulo(im1, im2, scale=1.0, offset=0)
            im_out.save("chops/subtract_modulo.png")

.. image:: images/compare_subtract_modulo.png
    :scale: 50%
    :align: center

