==========================
ImageChops multiply
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.multiply

----

Multiply
---------------------------

| Use the ``ImageChops.multiply(image1, image2)`` method to overlay 2 images of the same size.
| If an image is multiplied with an image with a solid black image, the result is black. 
| If an image is multiplied with a solid white image, the image is unaffected.
| out = image1 * image2 / MAX

.. code-block:: python

    from PIL import Image, ImageChops


    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.multiply(im1, im2)
            im_out.save("chops/multiply.png")


.. image:: images/compare_multiply.png
    :scale: 50%
    :align: center
