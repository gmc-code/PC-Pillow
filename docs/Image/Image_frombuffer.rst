==========================
Image frombuffer
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.frombuffer

----

Frombuffer
----------------------------

| Use the ``frombuffer(mode, size, data, decoder_name='raw', *args)`` to return an image referencing pixel data in a byte buffer.

| This function is similar to frombytes(), but uses data in the byte buffer, where possible. This means that changes to the original buffer object are reflected in this image. 
| Supported modes include "L", "RGBX", "RGBA", and "CMYK".
| Note that this function decodes pixel data only, not entire images. If you have an entire image file in a string, wrap it in a BytesIO object, and use open() to load it.
| mode - The image mode. See: Modes.
| size - The image size.
| data - A bytes or other buffer object containing raw data for the given mode.
| decoder_name - What decoder to use.
| args -Additional parameters for the given decoder. For the default encoder (“raw”), it's recommended that you provide the full set of parameters.

----

Frombuffer image
----------------------------

| The code below has bytes for 8 pixels that are then repeated to fill an image of size 64 x 64.


.. code-block:: python

    from PIL import Image


    data = bytearray(b'\x00\x00\x50\x50\xff\xff\x50\x50') * 128 * 4

    im = Image.frombuffer("L", (64, 64), data, 'raw', "L", 0, 1)
    im.save("images/Image_frombuffer.png")


.. image:: images/Image_frombuffer.png
    :scale: 50%
    :align: center
    