==========================
Image new
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.new

----

New
--------------


| Use ``Image.new(mode, size, color=0)`` to return a new image with the given mode and size and color.
| mode - The mode to use for the new image is usually one of ["1", "L", "RGB", "RGBA"]
| size - A 2-tuple, containing (width, height) in pixels.
| color - Default is black. If given, this should be a single integer or floating point value for single-band modes, and a tuple for multi-band modes (one value per band). When creating RGB images, you can also use color strings as supported by the ImageColor module. If the color is None, the image is not initialised.

----

Blank new png
----------------

| The code below saves a blank png of size (256, 256).

.. code-block:: python

    from PIL import Image

    new_im = Image.new("RGBA", (256, 256))
    new_im.save("new_images/blank.png")

----

Black new png
----------------

| The code below saves a white png of size (256, 256).

.. code-block:: python

    from PIL import Image

    new_im = Image.new("RGBA", (256, 256), (0, 0, 0))
    new_im.save("new_images/black.png")


.. image:: images/black.png
    :scale: 50%
    :align: center

----

Coloured new png
------------------

| The code below saves a light blue png of size (256, 256).

.. code-block:: python

    from PIL import Image

    new_im = Image.new("RGBA", (256, 256), (204, 229, 255))
    new_im.save("new_images/light_blue.png")


.. image:: images/light_blue.png
    :scale: 50%
    :align: center

----

Coloured new jpg
------------------

| The code below saves a green jpg of size (128, 128).

.. code-block:: python

    from PIL import Image

    new_im = Image.new("RGB", (128, 128), (0, 255, 0))
    new_im.save("new_images/green.jpg")


.. image:: images/green.jpg
    :scale: 50%
    :align: center

----

Greyscale new jpg
------------------

| The code below saves a grey jpg of size (128, 128).

.. code-block:: python

    from PIL import Image

    new_im = Image.new("L", (128, 128), (128))
    new_im.save("new_images/grey.jpg")


.. image:: images/grey.jpg
    :scale: 50%
    :align: center

