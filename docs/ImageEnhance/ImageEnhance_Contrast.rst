==========================
ImageEnhance Contrast
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageEnhance.html#PIL.ImageEnhance.Contrast

----

Contrast
----------------------

| Use the ``ImageEnhance.Contrast(image).enhance(factor)`` method to return an image with adjusted contrast.

.. py:function:: ImageEnhance.Contrast(image).enhance(factor)

    | **factor** is a floating point value controlling the enhancement. There are no restrictions on this value.
    | Factor 1.0 always returns a copy of the original image.
    | lower factors mean less contrast, and higher values more.


.. code-block:: python

    from PIL import Image, ImageEnhance


    with Image.open("test_images/alph_blocks.png") as im:
        new_im = ImageEnhance.Contrast(im).enhance(0.5)
        new_im.save("enhanced/contrast0_5.png")
        new_im = ImageEnhance.Contrast(im).enhance(0.8)
        new_im.save("enhanced/contrast0_8.png")
        new_im = ImageEnhance.Contrast(im).enhance(1)
        new_im.save("enhanced/contrast1.png")
        new_im = ImageEnhance.Contrast(im).enhance(1.3)
        new_im.save("enhanced/contrast1_3.png")
        new_im = ImageEnhance.Contrast(im).enhance(2)
        new_im.save("enhanced/contrast2.png")




.. image:: images/enhanced_contrast.png
    :scale: 40%
    :align: center

|  

.. image:: gifs/contrast.gif
    :scale: 50%
    :align: center
        
