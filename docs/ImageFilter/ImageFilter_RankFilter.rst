==========================
ImageFilter RankFilter
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageFilter.html

----

RankFilter
----------------------

| Use the ``Image.filter(ImageFilter.RankFilter(size, rank))`` method to use the chosen rank of pixel values in a pixel area given by the size.
| The rank filter sorts all pixels in a window of the given size, and returns the rank'th value.
| **size** - The kernel size, in pixels.
| **rank** - What pixel value to pick. Use 0 for a min filter, size * size / 2 for a median filter, size * size - 1 for a max filter, etc.

.. code-block:: python

    from PIL import Image, ImageFilter

   
    with Image.open("test_images/river_valley.jpg") as im:
        new_im = im.filter(ImageFilter.RankFilter(size=3, rank=1))
        new_im.save("filters/RankFilter1.png")
        new_im = im.filter(ImageFilter.RankFilter(size=3, rank=2))
        new_im.save("filters/RankFilter2.png")


.. image:: images/compare_RankFilter.png
    :scale: 50%
    :align: center



