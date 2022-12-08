==========================
ImageFilter MinFilter
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.MinFilter

----

MinFilter
----------------------

| Use the ``Image.filter(ImageFilter.MinFilter(radius=3))`` method to use the min pixel value in a pixel area given by the radius.

.. code-block:: python

    from PIL import Image, ImageFilter

   
    with Image.open("test_images/river_valley.jpg") as im:
        new_im = im.filter(ImageFilter.MinFilter(size=3))
        new_im.save("filters/MinFilter.png")

| Unfiltered, MinFilter, MedianFilter, ModeFilter and MaxFilter are compared below:

.. image:: images/compare_Filters.png
    :scale: 25%
    :align: center



