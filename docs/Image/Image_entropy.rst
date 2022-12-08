==========================
Image entropy
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.entropy

| Entropy is a statistical measure of randomness that can be used to characterize the texture of the input image.

----

Entropy
----------------------------

| Use the ``Image.entropy(mask=None, extrema=None)`` method to return a float value representing the image entropy.
| If a mask is provided, the method employs the histogram for those parts of the image where the mask image is non-zero. The mask image must have the same size as the image, and be either a bi-level image (mode 1) or a greyscale image (L).
| extrema - An optional tuple of manually-specified extrema for the minimum and maximum pixel values for each band in the image.


.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        print(im.entropy())
        # 2.5
    