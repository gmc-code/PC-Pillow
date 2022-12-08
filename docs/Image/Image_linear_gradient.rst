==========================
Image linear_gradient
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.linear_gradient

----

Linear_gradient
----------------------------

| Use ``Image.linear_gradient(mode)`` to generate 256x256 linear gradient from black to white, top to bottom.
| Input mode is from ["L", "P"].

.. code-block:: python

    from PIL import Image

    im = Image.linear_gradient('L')
    im.save("image/Image_linear_gradient.png")

.. image:: images/Image_linear_gradient.png
    :scale: 50%
    :align: center
    
