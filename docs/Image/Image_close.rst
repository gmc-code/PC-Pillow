==========================
Image close
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.close

----

Close
------------------------------

| Use the ``Image.close()`` method to close the file pointer. 
| This operation will destroy the image core and release its memory. The image data will be unusable afterward.
| This function is required to close images that have multiple frames or have not had their file read and closed by the load() method.

| In the code below, a jpg is opened and modified, **in place**, then saved, then closed.

.. code-block:: python

    from PIL import Image

    im = Image.open('shapes_jpgs/x.jpg')
    im.draft("L", (im.width // 2, im.height // 2))
    im.show()
    im.save("shapes_jpgs/box_half_grey.png")
    im.close()

    

