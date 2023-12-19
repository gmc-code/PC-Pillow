==========================
Image seek
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.seek

----

Seek
----------------------------

| Use the ``Image.seek(frame)`` method to seek to the given frame in the sequence file, such as a gif. 
| The method raises an EOFError exception if you seek beyond the end of the sequence. 
| When a sequence file is opened, the library automatically seeks to frame 0.
| frame - Frame number, starting at 0.

| ``Image.n_frames`` returns the number of frames.

----

Seek and save each frame
--------------------------

| The code below seeks to each frame and saves it as an RGB image.

.. code-block:: python

    from PIL import Image

    with Image.open("new_gifs/transform_tilt_x.gif") as im_gif:
        last_frame = im_gif.n_frames
        # im_gif.show()
        # convert RGB before save as jpeg to avoid "IOError: cannot write mode P as JPEG"

        for i in range(last_frame): 
            im_gif.seek(i)
            im_gif.convert("RGB").save("image/gifs/gif_frame" + str(i) + ".png")


