==========================
Image histogram
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.histogram

----

Histogram
----------------------------

| Use the ``Image.histogram(mask=None, extrema=None)`` method to return a histogram for the image. 
| mask - An optional mask.
| extrema -  An optional tuple of manually-specified extrema.
| The histogram is returned as a list of pixel counts, one for each pixel value in the source image. Counts are grouped into 256 bins for each band, even if the image has more than 8 bits per band. If the image has more than one band, the histograms for all bands are concatenated (for example, the histogram for an "RGB" image contains 768 values).
| A bilevel image (mode "1") is treated as a greyscale ("L") image by this method.
| If a mask is provided, the method returns a histogram for those parts of the image where the mask image is non-zero. The mask image must have the same size as the image, and be either a bi-level image (mode "1") or a greyscale image ("L").


| The code below prints the hsitogram for the Red channel of the image.

.. code-block:: python

    from PIL import Image

    with Image.open("shapes/box.png") as im:
        r, g, b = im.split()
        print(im.histogram(r))
        



