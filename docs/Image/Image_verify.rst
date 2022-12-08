==========================
Image verify
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.verify

----

Verify
----------------------------

| Use the ``Image.open(img_file).verify()`` method to verify the contents of a file. 
| For data read from a file, this method attempts to determine if the file is broken, without actually decoding the image data. 
| If this method finds any problems, it raises suitable exceptions. 
| If you need to load the image after using this method, you must reopen the image file.

| The verify_response if None for a valid file.

----

Verify image file
----------------------------

| The code below verifies a image file.

.. code-block:: python

    from PIL import Image
    from urllib.request import urlopen

    def get_verify(img_file):
        try:
            verify_response = Image.open(img_file).verify()
            print(f'{verify_response} was returned by verify')
            im = Image.open(img_file)
            print(f'{im.filename.split("/")[-1]} is a valid image')
            # im.show()
        except Exception:
            print('Invalid image')


    get_verify("test_images/alph_blocks.png")
    get_verify("test_images/AtoZ.jpg")


----

Verify image url
----------------------------

| The code below verifies a image at a url.

.. code-block:: python

    from PIL import Image
    from urllib.request import urlopen

    def get_verify_url(img_file):
        try:
            verify_response = Image.open(urlopen(img_file)).verify()
            print(f'{verify_response} was returned by verify')
            im = Image.open(urlopen(img_file))
            filename = img_file.split("/")[-1]
            print(f'{filename} is a valid image')
            # im.show()
        except Exception:
            print('Invalid image')


    url = "https://pc-pillow.readthedocs.io/en/latest/_images/tri.png"
    get_verify_url(url)

