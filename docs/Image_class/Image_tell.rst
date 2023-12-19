==========================
Image tell
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.tell

----

Tell
----------------------------

| Use the ``Image.tell()`` method to return the current frame number, starting at 0, in the sequence file, such as a gif.


.. code-block:: python

    from PIL import Image

    with Image.open("new_gifs/transform_tilt_x.gif") as im_gif:
        print(im_gif.tell())
        # 0

