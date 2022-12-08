==========================
ImageChops composite
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.composite
| See: Image.composite()

----

Composite
---------------------------

| Alias for ``Image.composite()``.
| Use the ``ImageChops.composite(image1, image2, mask)`` method to create a composite image by blending images using a transparency mask. Here, mask is another image which remains transparent.
| The second image, must have the same mode and size as the first image. 
| The mask image can have mode "1", "L", or "RGBA", and must have the same size as the other two images.


| In the example below the mask goes from black, 0 (fully transparent) to white, 255 (fully opaque) from left to right.
| image1 follows the mask transparency.
| image2 follows the mask transparency in reverse. 

.. code-block:: python

    from PIL import Image, ImageChops

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            with Image.open("test_images/greyscale_vert_gradient_32.png") as mask:
                im_out = ImageChops.composite(im1, im2, mask)
                im_out.save("chops/composite.png")



.. image:: images/compare_composite.png
    :scale: 50%
    :align: center


