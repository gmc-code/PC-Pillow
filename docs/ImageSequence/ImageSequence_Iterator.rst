==========================
ImageSequence Iterator
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageSequence.html#PIL.ImageSequence.Iterator

----

Iterator
----------------------------

| Use the ``ImageSequence.Iterator(im)`` class to implement an iterator object that can be used to loop over an image sequence such as a gif.
| You can use the [] operator to access elements by index. This operator will raise an IndexError if you try to access a nonexistent frame.
| **im** - An image object.

----

Save each frame
--------------------------

| The code below iterates over each frame and saves it as a png image.

.. code-block:: python

    from PIL import Image, ImageSequence


    with Image.open("gifs/transform_tilt_x.gif") as im_gif:
        index = 0
        for frame in ImageSequence.Iterator(im_gif):
            frame.save(f"images/gif_frame_is_{index}.png")
            index += 1



.. image:: gifs/transform_tilt_x.gif
    :scale: 50%
    :align: center

.. image:: images/gif_frame_is_0.png
    :scale: 50%
    :align: center

.. image:: images/gif_frame_is_7.png
    :scale: 50%
    :align: center

.. image:: images/gif_frame_is_15.png
    :scale: 50%
    :align: center

