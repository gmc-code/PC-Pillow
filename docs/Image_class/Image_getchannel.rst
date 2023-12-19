==========================
Image getchannel
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getchannel

----

Getchannel
----------------------------

| Use the ``Image.getchannel(channel)`` returns an image, in "L" mode (greyscale), containing a single channel of the source image.
| channel - Could be index (0 for "R" channel of "RGB") or channel name ("A" for alpha channel of "RGBA").


.. code-block:: python

    from PIL import Image

    with Image.open("test_images/alph_blocks.png") as im:
        im1 = im.getchannel("R")
        # im1.show()
        im1.save("Image/Image_channel_R.png")
        im1 = im.getchannel("G")
        # im1.show()
        im1.save("Image/Image_channel_G.png")
        im1 = im.getchannel("B")
        # im1.show()
        im1.save("Image/Image_channel_B.png")
    

.. image:: images/compare_channel.png
    :scale: 50%
    :align: center


                


