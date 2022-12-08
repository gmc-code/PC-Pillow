==========================
ImageChops duplicate
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.duplicate
| See: Image.copy()

----

Duplicate
---------------------------

| Alias for ``Image.copy()``.
| Use the ``ImageChops.duplicate(image)`` method to copy an image. 
| The code below first duplciates an image so a copy can be converted to greyscale.

.. code-block:: python

    from PIL import Image, ImageChops


    def get_greyscale(img):
        imgd = ImageChops.duplicate(img)
        return imgd.convert('L')

    with Image.open("test_images/crosses.png") as im1:
        im1g = get_greyscale(im1)
        im1g.save("chops/duplicate.png")


.. image:: images/compare_duplicate.png
    :scale: 50%
    :align: center


