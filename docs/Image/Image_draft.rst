==========================
Image draft
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.draft

----

Draft
-----------

| Use the ``Image.draft(mode, size)`` method modifies the Image object **in place** to convert a JPEG to the given mdoe at the given size.

| In the code below, a jpg is opened and modified, **in place**, then saved, then closed.

.. code-block:: python

    from PIL import Image

    im = Image.open('shapes_jpgs/x.jpg')
    im.draft("L", (im.width // 2, im.height // 2))
    im.show()
    im.save("shapes_jpgs/x_half_grey.png")
    im.close()


.. image:: images/compare_draft.png
    :scale: 50%
    :align: center
    
