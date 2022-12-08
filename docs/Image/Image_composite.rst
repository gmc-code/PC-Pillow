==========================
Image composite
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.composite
| See: ImageChops.composite()

----

Composite
---------------------------

| Use the ``Image.composite(image1, image2, mask)`` method to return a composite image by blending images using a transparency mask. 
| The mask is another image which remains transparent.
| The second image, must have the same mode and size as the first image. 
| The mask image can have mode "1", "L", or "RGBA", and must have the same size as the other two images.

----

Composite with stepped transparency mask
-------------------------------------------

| In the example below the mask goes from black, 0 (fully transparent) to white, 255 (fully opaque) from left to right in sections of 32 pixels.
| im1 follows the mask transparency.
| im2 follows the mask transparency in reverse. 

.. code-block:: python

    from PIL import Image

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            with Image.open("test_images/greyscale_vert_gradient_32.png") as mask:
                im_out = Image.composite(im1, im2, mask)
                im_out.save("Image/compare_composite.png")



.. image:: images/compare_composite.png
    :scale: 50%
    :align: center


----

Composite with stepped transparency mask
-------------------------------------------

| In the example below the mask goes from black, in the center to white at the edges.
| im1 follows the mask transparency.
| im2 follows the mask transparency in reverse. 

.. code-block:: python

    from PIL import Image

with Image.open("test_images/crosses.png") as im1:
    with Image.open("test_images/circles.png") as im2:
        with Image.open("test_images/linear_gradient.png") as mask:
            im_out = Image.composite(im1, im2, mask)
            im_out.save("Image/Image_composite2.png")


.. image:: images/compare_composite2.png
    :scale: 50%
    :align: center

----

Composite with radial gradient mask
-------------------------------------------


| In the example below the mask goes from black, in the center to white at the edges.
| im1 follows the mask transparency.
| im2 follows the mask transparency in reverse. 

.. code-block:: python

    from PIL import Image

    with Image.open("test_images/crosses.png") as im1:
        with Image.open("test_images/circles.png") as im2:
            with Image.open("test_images/radial_gradient.png") as mask:
                im_out = Image.composite(im1, im2, mask)
                im_out.save("Image/Image_composite3.png")


.. image:: images/compare_composite3.png
    :scale: 50%
    :align: center

