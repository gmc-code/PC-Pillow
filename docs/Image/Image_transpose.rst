==========================
Image transpose
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.transpose

----

Transpose
----------------------------

| Use the ``Image.transpose(method)`` method to rotate or flip an image using method constants.

----

Transpose variations
----------------------------

| The various flip and rotate methods are below.
| All 7 variations of the original by flipping and/or rotating are below.
| Transpose.TRANSPOSE is the equivalent of rotating 270 and flipping left to right.
| Transpose.TRANSVERSE is the equivalent of rotating 90 and flipping left to right.

----

Transpose.FLIP_LEFT_RIGHT
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.FLIP_LEFT_RIGHT)
        im2.save("transpose/flip_lr.png")


.. image:: images/compare_transpose_flip_lr.png
    :scale: 50%
    :align: center

----

Transpose.FLIP_TOP_BOTTOM
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.FLIP_TOP_BOTTOM)
        im2.save("transpose/flip_tb.png")


.. image:: images/compare_transpose_flip_tb.png
    :scale: 50%
    :align: center

----

Transpose.ROTATE_90
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
       im2 = im.transpose(method=Image.Transpose.ROTATE_90)
        im2.save("transpose/r_90.png")
        
.. image:: images/compare_transpose_r_90.png
    :scale: 50%
    :align: center

----

Transpose.ROTATE_180
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.ROTATE_180)
        im2.save("transpose/r_180.png")


.. image:: images/compare_transpose_r_180.png
    :scale: 50%
    :align: center

----

Transpose.ROTATE_270
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.ROTATE_270)
        im2.save("transpose/r_270.png")
    

.. image:: images/compare_transpose_r_270.png
    :scale: 50%
    :align: center

----

Transpose.TRANSPOSE
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.TRANSPOSE)
        im2.save("transpose/tp.png")


.. image:: images/compare_transpose_tp.png
    :scale: 50%
    :align: center

----

Transpose.TRANSVERSE
----------------------------------

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/shapes.png") as im:
        im2 = im.transpose(method=Image.Transpose.TRANSVERSE)
        im2.save("transpose/tv.png")

.. image:: images/compare_transpose_tv.png
    :scale: 50%
    :align: center




    

