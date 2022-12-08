==========================
Image copy
==========================


| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.copy
| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.duplicate

----

Copy
---------------------------

| Use the ``Image.copy()`` method to copy an image. Use this method if you wish to paste things into an image, but still retain the original.
| The code below first copies an image so the copy can be converted to greyscale.

.. code-block:: python

    from PIL import Image


    def get_greyscale(img):
        imgd = img.copy()
        return imgd.convert('L')

    with Image.open("test_images/crosses.png") as im:
        im1g = get_greyscale(im)
        im1g.save("image/copy.png")
  

.. image:: images/compare_copy.png
    :scale: 50%
    :align: center


