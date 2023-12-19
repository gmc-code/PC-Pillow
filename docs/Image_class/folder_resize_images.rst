==========================
Resize an image folder
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.resize

----

Resize a folder using thumbnail
---------------------------------

| The code below resizes images in the **shapes** folder to the **shapes_128** folder.
| The code, **im.thumbnail(thumb_size)**, modifies the image **in place**. 
| The **copy()** method should be used to return a copy of the images first.


.. code-block:: python

    from PIL import Image
    from pathlib import Path

    thumb_size = (128, 128)
    im_dir = "shapes"
    im_new_dir = "shapes_128"
    cwd = Path.cwd()
    shapes = cwd / im_dir
    shape_files = shapes.iterdir()
    new_shapes = cwd / im_new_dir
    if not(new_shapes.exists()):
        new_shapes.mkdir()

    for f in shape_files:
        if f.suffix == ".jpg" or f.suffix == ".png":
            with Image.open(im_dir + "/" + f.name) as im_orig:
                im = im_orig.copy()
                im.thumbnail(thumb_size)
                im.save(im_new_dir + "/" + f.name)



