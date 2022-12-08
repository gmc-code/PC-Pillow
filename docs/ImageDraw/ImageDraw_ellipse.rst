==========================
ImageDraw ellipse
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.ellipse

----

Ellipse
----------------------

| Use the ``ImageDraw.ellipse(xy, fill=None, outline=None, width=1)`` method to draw an ellipse inside the given bounding box.

.. py:function:: ImageDraw.ellipse(xy, fill=None, outline=None, width=1)

    | **xy** - Two points to define the bounding box. Sequence of [(x0, y0), (x1, y1)] or [x0, y0, x1, y1], where x1 >= x0 and y1 >= y0.
    | **fill** - Color to use for the fill.
    | **outline** - Color to use for the outline.
    | **width** - The line width, in pixels.

| The code below draws a blue ellipse with a yellow fill.

.. code-block:: python

    from PIL import Image, ImageDraw

    im = Image.new('RGB', (256, 256), "white")
    drw = ImageDraw.Draw(im, 'RGB')

    drw.ellipse(xy=(20, 40, 236, 116), fill="yellow", outline="blue", width=5)
    # im.show()
    im.save("ImageDraw/ImageDraw_ellipse.jpg")


.. image:: images/ImageDraw_ellipse.jpg
    :scale: 50%
    :align: center



