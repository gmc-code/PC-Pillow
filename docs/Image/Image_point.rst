==========================
Image point
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.point

----

Point
----------------------------

| Use the ``Image.point(lut, mode=None)`` to return an image from mapping the image through a lookup table or function.
| lut - A lookup table, containing 256 (or 65536 if mode=="I" or "L") values per band in the image. 
| A function can be used instead, it should take a single argument. The function is called once for each possible pixel value, and the resulting table is applied to all bands of the image.
| mode - Output mode (default is same as input). This can only be used if the source image has mode "L" or "P", and the output has mode "1" or the source image mode is "I" and the output mode is "L".


.. code-block:: python

    from PIL import Image

    def func_light(x):
        return x + 55

    def func_inv(x):
        return 255 - x

    with Image.open("test_images/rhino.jpg") as im:
        im1 = im.point(func_light)
        im1.show()
        im1.save("Image/Image_point_light.png")
        im2 = im.point(func_inv)
        im2.show()
        im2.save("Image/Image_point_inv.png")

    

.. image:: images/compare_point.png
    :scale: 50%
    :align: center


                


