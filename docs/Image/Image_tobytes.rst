==========================
Image tobytes
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.tobytes

| For internal use.

----

Tobytes
----------------------------

| Use the ``Image.tobytes(encoder_name='raw', *args)`` method to return an image as a bytes object.
| This method returns the raw image data from the internal storage. For compressed image data (e.g. PNG, JPEG) use save(), with a BytesIO parameter for in-memory data.
| args - Extra arguments to the encoder.

