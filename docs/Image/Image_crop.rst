==========================
Image crop
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.crop

----

Crop 
----------------------------

| Use the ``Image.crop(box=None)`` method to crop an image. 
| box - The crop rectangle, as a (left, upper, right, lower) tuple.
| The box can be larger than the original image, including negative left and upper.

----

Crop smaller
----------------------------

| Crop can be used to crop the image to make it smaller.

.. code-block:: python

    from PIL import Image

    with Image.open("test_images/shapes.png") as im:
        cropx, cropy = 32, 32
        box = (cropx, cropy, im.width - cropx, im.height - cropy)
        im_new = im.crop(box)
        im_new.save("image/image_crop.png")

.. image:: images/compare_crop.png
    :scale: 50%
    :align: center

----

Crop larger
------------------

| Crop can be used to expand the image in any direction.

.. code-block:: python

    from PIL import Image  

    with Image.open("test_images/shapes.png") as im:
        cropx, cropy = -64, -64
        box = (cropx, cropy, im.width - cropx, im.height - cropy)
        im_new = im.crop(box)
        im_new.save("image/image_crop_expand.png")

.. image:: images/compare_crop_expand.png
    :scale: 50%
    :align: center
