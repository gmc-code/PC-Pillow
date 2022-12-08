==========================
ImageChops blend
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.blend
| See: Image.blend()
----

Blend
---------------------------

| Use the ``ImageChops.blend(image1, image2, alpha)`` method to blend images using constant transparency weight. Alias for ``.Image.blend()``
| The second image, must have the same mode and size as the first image. 
| If alpha is 0.0, a copy of the first image is returned. If alpha is 1.0, a copy of the second image is returned. There are no restrictions on the alpha value. If necessary, the result is clipped to fit into the allowed output range.

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            im_out = ImageChops.blend(im1, im2, 0.5)
            im_out.save("chops/blend.png")

.. image:: images/compare_blend.png
    :scale: 50%
    :align: center


