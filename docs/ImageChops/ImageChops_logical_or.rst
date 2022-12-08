==========================
ImageChops logical_or
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageChops.html#PIL.ImageChops.logical_or

----

Logical_or
---------------------------

| Use the ``ImageChops.logical_or(image1, image2)`` method to return an image that is a Logical OR between two images.
| Both of the images must have mode "1".

| The code below, first converts the images to black and white by first converting to greyscale using .convert('L'). Then the .point(point_function, mode='1') method is used to convert to black and white.
| out = ((image1 or image2) % MAX)


.. code-block:: python

    from PIL import Image, ImageChops


    def point_function(x):
        if x > 254:
            return 255
        else:
            return 0


    def get_black_and_white(img):
        imgd = ImageChops.duplicate(img)
        return imgd.convert('L').point(point_function, mode='1')


    with Image.open("test_images/crosses.png") as im1:
        im1bw = get_black_and_white(im1)
        with Image.open("test_images/circles.png") as im2:
            im2bw = get_black_and_white(im2)
            im_out = ImageChops.logical_or(im1bw, im2bw)
            im_out.save("chops/logical_or.png")


.. image:: images/compare_logical_or.png
    :scale: 50%
    :align: center


