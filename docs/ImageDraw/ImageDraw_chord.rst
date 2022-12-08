==========================
ImageDraw chord
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.chord

----

Chord
----------------------

| Use the ``ImageDraw.chord(xy, start, end, fill=None, outline=None, width=1)`` to connect the end points of an imaginary arc with a straight line.

.. py:function:: ImageDraw.chord(xy, start, end, fill=None, outline=None, width=1)
    
    | **xy** - Two points to define the bounding box. Sequence of [(x0, y0), (x1, y1)] or [x0, y0, x1, y1], where x1 >= x0 and y1 >= y0.
    | **start** - Starting angle, in degrees. Angles are measured from 3 o'clock, increasing clockwise.
    | **end** - Ending angle, in degrees.
    | **fill** - Color to use for the fill.
    | **outline** - Color to use for the outline.
    | **width** - The line width, in pixels.

| The code below draws a blue chord across an arc, and fills it lightgreen.

.. code-block:: python

    from PIL import Image, ImageDraw

    im = Image.new('RGB', (256, 256), "white")
    drw = ImageDraw.Draw(im, 'RGB')

    drw.chord(xy=(20, 40, 236, 216), start=0, end=180, fill="lightgreen", outline="blue", width=10)
    # im.show()
    im.save("ImageDraw/ImageDraw_chord.jpg")


.. image:: images/ImageDraw_chord.jpg
    :scale: 50%
    :align: center



