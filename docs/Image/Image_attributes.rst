==========================
Image attributes
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#image-attributes

| See docs for other info that is available apart from examples below.

----

Image info
----------------------

| The code below shows how to open an image and print out some info about it.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.filename, im.format, im.mode, im.size, im.width, im.height, sep="; ")

    with Image.open("shapes_jpgs/box.jpg") as im:
        print(im.filename, im.format, im.mode, im.size, im.width, im.height, sep="; ")

| The first printout is: shapes/box.png; PNG; RGBA; (256, 256); 256; 256
| The second printout is: shapes_jpgs/box.jpg; JPEG; RGB; (256, 256); 256; 256

# shapes/box.png; PNG; RGBA; (256, 256); 256; 256
# shapes_jpgs/box.jpg; JPEG; RGB; (256, 256); 256; 256


