==========================
ImageFilter ModeFilter
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html#PIL.ImageFilter.ModeFilter

----

ModeFilter
----------------------

| Use the ``Image.filter(ImageFilter.ModeFilter(radius=3))`` method to use the mode of the pixel value in a pixel area given by the radius.
| Picks the most frequent pixel value in a box with the given size. Pixel values that occur only once or twice are ignored; if no pixel value occurs more than twice, the original pixel value is preserved.

.. code-block:: python

    from PIL import Image, ImageFilter

   
    with Image.open("test_images/river_valley.jpg") as im:
        new_im = im.filter(ImageFilter.ModeFilter(size=3))
        new_im.save("filters/ModeFilter.png")

| Unfiltered, MinFilter, MedianFilter, ModeFilter and MaxFilter are compared below:

.. image:: images/compare_Filters.png
    :scale: 25%
    :align: center



