==========================
Convert a folder
==========================

| For pathlib and os use See: https://csatlas.com/python-list-directory/

----

Convert a folder to jpgs using pathlib
-------------------------------------------

| See: https://docs.python.org/3/library/pathlib.html

| Use the built in **pathlib** library for the file handling.
| Convert pngs to jpgs and save in the new folder.

| Get the current working directory, cwd, with **Path.cwd()**.
| Create the path to the shapes folder: **cwd / "shapes"**.
| List the files in the shapes folder: **shapes.iterdir()**
| Build the path to the new directory for the converted files: **cwd / "shapes_jpgs"**
| After checking that it does not already exist, make the new directory for the converted files: **new_shapes.mkdir()**
| Get the file extension via: **f.suffix**
| Get the file name via: **f.name**
| Get the file name without the extension via: **f.stem**


.. code-block:: python

    from PIL import Image
    from pathlib import Path

    im_dir = "shapes"
    im_new_dir = "shapes_jpgs"
    cwd = Path.cwd()
    shapes = cwd / im_dir
    shape_files = shapes.iterdir()
    new_shapes = cwd / im_new_dir
    if not(new_shapes.exists()):
        new_shapes.mkdir()
    for f in shape_files:
        if f.suffix == ".png":
            with Image.open(im_dir + "/" + f.name) as im:
                new_im = im.convert('RGB')
                new_im.save(im_new_dir + "/" + f.stem + ".jpg")


| Use the glob method to just get files with matching file extension.

.. code-block:: python

    from PIL import Image
    from pathlib import Path

    im_dir = "shapes"
    im_new_dir = "shapes_jpgs"
    imgs_path = Path.cwd() / im_dir
    new_imgs_path = Path.cwd() / im_new_dir

    if not(new_imgs_path.exists()):
        new_imgs_path.mkdir()

    for f in imgs_path.glob('*.png'):
        with Image.open(f) as im:
            save_path = new_imgs_path / (f.stem + '.jpg')
            rgb_im2 = im.convert('RGB')
            rgb_im2.save(save_path, quality=95)


----

Convert a folder to jpgs using os
---------------------------------------

| See: https://docs.python.org/3/library/pathlib.html

| Use the built in **os** library for the file handling.
| Convert pngs to jpgs and save in the new folder.

| List the files in the shapes folder: **os.listdir(im_dir)**
| After checking that it does not already exist, make the new directory for the converted files: **os.mkdir(im_new_dir)**
| Check that the file is a png file via: **f.endswith(".png")**
| Get the file name without the extension via: **fn, fext = os.path.splitext(f)**

.. code-block:: python

    from PIL import Image
    import os

    im_dir = "shapes"
    im_new_dir = "shapes0_jpgs"
    shape_files = os.listdir(im_dir)

    if not(os.path.exists(im_new_dir)):
        os.mkdir(im_new_dir)

    for f in shape_files:
        if f.endswith(".png"):
            with Image.open(im_dir + "/" + f) as im:
                new_im = im.convert('RGB')
                fn, fext = os.path.splitext(f)
                new_im.save(im_new_dir + "/" + fn + ".jpg")
