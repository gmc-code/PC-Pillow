==========================
ImageDraw fontmode
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.fontmode

----

Fontmode
----------------------

| Use the ``ImageDraw.fontmode`` attribute to set or return the current font drawing mode. 
| Set to "1" to disable antialiasing or "L" to enable antialiasing.

| Then the image is saved.

.. code-block:: python

    from PIL import Image, ImageDraw, ImageFont

    fnt = ImageFont.truetype("C:/Windows/Fonts/Segoeui.ttf", 72)
    with Image.open("test_images/shapes.jpg") as im:
        drw = ImageDraw.Draw(im)
        print(drw.fontmode)  # L
        text = "Shapes"
        drw.text((2, 0), text=text, font=fnt, fill=(0, 0, 255))
        drw.fontmode = "I"
        print(drw.fontmode)  # I
        drw.text((2, 100), text=text, font=fnt, fill=(0, 0, 255))
        # im.save("ImageDraw/ImageDraw_fontmode.png")
        im.show()


.. image:: images/ImageDraw_fontmode.png
    :scale: 50%
    :align: center
