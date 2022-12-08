==========================
Image show
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.show

----

Show
----------------------

| Use the ``.show()`` method to open the image using the default app. 
| In Windows, the default app is usually Photos.

| The code below opens an image and shows it.
| A temporary file is created for display.

.. code-block:: python

    from PIL import Image

    with Image.open("tri.jpg") as im:
        im.show()
         

    
            
