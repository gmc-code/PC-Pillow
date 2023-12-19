==========================
Image open
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.open
| See: https://pillow.readthedocs.io/en/stable/reference/open_files.html#file-handling

----

Open file in the same folder
------------------------------

| The code below opens an image and shows it.
| Use **with** to automatically close the file resource.
| To refer to the image object as **im**, use **as im**.
| The file below is assumed to be in the same folder as the python script.

.. code-block:: python

    from PIL import Image

    with Image.open("tri.png") as im:
        im.show()

.. image:: images/tri.png
    :scale: 50%
    :align: center
    
----

Open file in a subfolder
---------------------------

| The file below is in the "shapes" folder within the folder containing the python script.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/tri.png") as im:
        im.show()

.. image:: images/tri.png
    :scale: 50%
    :align: center
    
----

Open file from a url
---------------------------

| The code below uses the **urllib.request** library to help open an image url.

.. code-block:: python

    from PIL import Image
    from urllib.request import urlopen

    url = "https://pc-pillow.readthedocs.io/en/latest/_images/tri.png"

    with Image.open(urlopen(url)) as im:
        im.show()

.. image:: images/tri.png
    :scale: 50%
    :align: center
    