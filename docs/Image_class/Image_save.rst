==========================
Image save
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.save

----

Save
-------

| Use the ``Image.save(file, format=None, **params)`` method to save the image under the given filename. If no format is specified, the format to use is determined from the filename extension, if possible.
| file - A filename (string), pathlib.Path object or file object. You can use a file object instead of a filename. In this case, you must always specify the format. The file object must implement the seek, tell, and write methods, and be opened in binary mode.
| format - Optional format override. If omitted, the format to use is determined from the filename extension. If a file object was used instead of a filename, this parameter should always be used.
| params - Extra parameters to the image writer.

----

Same file type
----------------

| The code below saves an image.

.. code-block:: python

    from PIL import Image

    with Image.open("arrows/Narrow.png") as im:
        im.save("arrows/arrow_0.png")     

----

Save as JPEG
--------------------
    
| The file extension in the new file name is used to specify the file type for saving.
| PNGs need to have the alpha channel removed to save the image as a jpg.
| Use the **.convert('RGB')** method to convert a png image to a jgp before attempting to save it.
| Use the **.save** method specifying the quality parameter as **quality=95** for best quality.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        new_im = im.convert('RGB')
        new_im.save("shapes/box.jpg", quality=95)

----

Save as PNG
--------------------
    
| The file extension in the new file name is used to specify the file type for saving.
| PNGs need to have the alpha channel removed to save the image as a jpg.
| **compress_level** is a number between 0 and 9: 1 gives best speed, 9 gives best compression, 0 gives no compression at all. Default is 6.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.jpg") as im:
        new_im.save("shapes/box.png", compress_level=9)

----

Saving gifs
-----------------

| See : https://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html#gif-saving

| The code below modifies all frames and saves them.

.. code-block:: python

    from PIL import Image, ImageSequence


    def addOverlay(frame):
        im = Image.open('image/ambulance_L.jpg')
        position = 'bottomRight'
        coords = {
            'topLeft': (0, 0),
            'bottomRight': (frame.width - im.width, frame.height - im.height)
        }
        frame.paste(im, coords[position])
        return frame

    with Image.open("new_gifs/transform_tilt_x.gif") as im_gif:
        # Run 'addOverlay' on each frame in the image
        frames = ImageSequence.all_frames(im_gif, addOverlay)
        # Save the frames as a new image
        frames[0].save('new_gifs/transform_tilt_x_overlay.gif', save_all=True, append_images=frames[1:])

