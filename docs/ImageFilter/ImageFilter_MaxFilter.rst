==========================
ImageFilter MaxFilter
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.MaxFilter

----

MaxFilter
----------------------

| Use the ``Image.filter(ImageFilter.MaxFilter(radius=3))`` method to use the max pixel value in a pixel area given by the radius.

.. code-block:: python

    from PIL import Image, ImageFilter

   
    with Image.open("test_images/river_valley.jpg") as im:
        new_im = im.filter(ImageFilter.MaxFilter(size=3))
        new_im.save("filters/MaxFilter.png")

| Unfiltered, MinFilter, MedianFilter, ModeFilter and MaxFilter are compared below:

.. image:: images/compare_Filters.png
    :scale: 25%
    :align: center



