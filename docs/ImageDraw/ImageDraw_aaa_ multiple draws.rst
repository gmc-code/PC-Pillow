==========================
ImageDraw_Draw
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.Draw
| See: https://www.blog.pythonlibrary.org/2021/02/23/drawing-shapes-on-images-with-python-and-pillow/
| For HTML colour names that can be used See: https://www.w3schools.com/tags/ref_colornames.asp

| The ImageDraw module provides simple 2D graphics for Image objects. You can use this module to create new images, annotate or retouch existing images, and to generate graphics on the fly for web use.

----

Draw
----------------------

| Import ImageDraw.
| Create the draw object: **ImageDraw.Draw(im, 'RGB')**

.. code-block:: python

    from PIL import Image, ImageDraw


    im = Image.new('RGB', (256, 256), "white")
    drw = ImageDraw.Draw(im, 'RGB')

    drw.ellipse((25, 50, 175, 200), fill="red")
    drw.ellipse((100, 150, 275, 300), outline="black", width=1,
                    fill="yellow")
    drw.line((25, 50, 175, 200), fill="blue", width=10)
    drw.del
    
    im.save("new_images/draw_examples.jpg")

.. image:: images/Color.gif
    :scale: 50%
    :align: center
        
