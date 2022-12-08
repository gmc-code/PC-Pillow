==========================
Image tobitmap
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.tobitmap
| See: https://wiki.multimedia.cx/index.php/XBM
| See: https://www.tau.ac.il/images/desc/Images.html

----

Tobitmap
----------------------------

| Use the ``Image.tobitmap(name='image')`` to return the mode 1 image converted to an X11 bitmap.
| name - The name prefix to use for the bitmap variables.
| It returns a string containing an X11 bitmap.

.. code-block:: python

    from PIL import Image
    from io import BytesIO


    im_L = Image.frombytes("L", (8, 8), b'''\
    \xff\xff\xff\xff\xff\xff\xff\xff\
    \xff\xff\x00\x00\x00\x00\xff\xff\
    \xff\x00\xff\x00\x00\xff\x00\xff\
    \xff\x00\x00\xff\xff\x00\x00\xff\
    \xff\x00\x00\xff\xff\x00\x00\xff\
    \xff\x00\xff\x00\x00\xff\x00\xff\
    \xff\xff\x00\x00\x00\x00\xff\xff\
    \xff\xff\xff\xff\xff\xff\xff\xff\
    ''')
    im_L = im_L.convert("1")
    im_xbm = im_L.tobitmap("xshape")  # "xbm" format (X11 bitmap)
    print(im_xbm.decode('ascii'))

    '''
    #define xshape_width 8
    #define xshape_height 8
    static char xshape_bits[] = {
    0xff,0xc3,0xa5,0x99,0x99,0xa5,0xc3,0xff
    };
    '''
----