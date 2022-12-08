==========================
ImageChops add
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.add

----

Add
---------------------------

| Use the ``ImageChops.add(image1, image2, scale=1.0, offset=0)`` method to add two images, dividing the result by scale and adding the offset.
| out = ((image1 + image2) / scale + offset)

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.add(im1, im2)
            im_out.save("chops/add.png")


.. image:: images/compare_add.png
    :scale: 50%
    :align: center
