==========================
Image getdata
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.getdata

----

Getdata
----------------------------

| Use the ``Image.getdata(band=None)`` method to return the contents of an image as a sequence object containing pixel values. 
| band - is the band to return. The default is to return all bands. To return a single band, pass in the index value (e.g. 0 to get the "R" band from an "RGB" image).

| The sequence object is flattened, so that values for line one follow directly after the values of line zero, and so on.
| Note that the sequence object returned by this method is an internal PIL data type, which only supports certain sequence operations. To convert it to an ordinary sequence (e.g. for printing), use list(im.getdata()).

----

Getdata to replace a colour
--------------------------------

| The code below replaces the transparent black, shown as white, with a pinkish transparent color.

.. code-block:: python
    
    from PIL import Image

    with Image.open("test_images/shapes.png") as im:
        im1 = im.convert(mode='RGBA')
        datas = im1.getdata()
        newData = []
        for pixel in datas:
            if pixel[0] == 0 and pixel[1] == 0 and pixel[2] == 0: # finding black colour by its RGB value
                # storing a transparent colour insetad of black
                newData.append((250, 160, 160, 155))
            else:
                newData.append(pixel) # other colours remain unchanged

        im1.putdata(newData)
        im1.save("Image/Image_getdata.png")


.. image:: images/compare_getdata.png
    :scale: 50%
    :align: center


