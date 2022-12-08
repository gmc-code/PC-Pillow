==========================
ImageDraw textlength
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.textlength

----

Draw
Rectangle
----------------------

| Use the ``ImageDraw.rectangle(xy, fill=None, outline=None, width=1)`` method to draw rectangle.

.. py:function:: ImageDraw.rectangle(xy, fill=None, outline=None, width=1)

    | **xy** - Two points to define the bounding box. Sequence of either [(x0, y0), (x1, y1)] or [x0, y0, x1, y1]. The bounding box is inclusive of both endpoints.
    | **fill** - Color to use for the fill.
    | **outline** - Color to use for the outline.
    | **width** - The line width, in pixels.

| The code below draws a blue line with no joint, and a red line with a curved joint.

.. code-block:: python

    from PIL import Image, ImageDraw


    im = Image.new('RGB', (256, 256), "white")
    drw = ImageDraw.Draw(im, 'RGB')

    box = [(10, 50), (240, 200)]

    drw.rectangle(xy=box, fill="red", outline="blue", width=30)
    # im.show()
    im.save("ImageDraw/ImageDraw_rectangle.jpg")


.. image:: images/ImageDraw_rectangle.jpg
    :scale: 50%
    :align: center
