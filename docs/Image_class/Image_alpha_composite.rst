==========================
Image alpha composite
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.alpha_composite

----

Alpha composite
----------------------------

| Use the ``Image.alpha_composite(image1, image2)`` method to return an image as a composite of image2 over image1.
| Fully transparent regions do not show in the resultant image.
| Both images must be the same size and both must have mode RGBA.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/x.png") as im1:
        with Image.open("shapes/o.png") as im2:
            # print(im1.mode, im2.mode)
            im_out = Image.alpha_composite(im1, im2)
            im_out.save("Image/Image_alpha_composite.png")


.. image:: images/Image_alpha_composite.png
    :scale: 50%
    :align: center
    
