==========================
ImageDraw textlength
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.textlength

----

Textlength
----------------------

| Use the ``ImageDraw.textlength(text, font=None, direction=None, features=None, language=None, embedded_color=False)`` method to return the length (in pixels as a float) of given text

.. py:function:: ImageDraw.textlength(text, font=None, direction=None, features=None, language=None, embedded_color=False)

    | **text** - Text to be measured. May not contain any newline characters.
    | **font** - An ImageFont.ImageFont instance such as ``ImageFont.truetype("C:/Windows/Fonts/Segoeui.ttf", 24)``
    | **direction** - Direction of the text. It can be ``"rtl"`` (right to left), ``"ltr"`` (left to right) or ``"ttb"`` (top to bottom). Requires **libraqm**.
    | **features** - A list of OpenType font features to be used during text layout. This is usually used to turn on optional font features that are not enabled by default, for example ``"dlig"`` or ``"ss01"``, but can be also used to turn off default font features, for example ``"-liga"`` to disable ligatures or ``"-kern"`` to disable kerning. Requires **libraqm**.
    | **language** - Language of the text. Different languages may use different glyph shapes or ligatures. This parameter tells the font which language the text is in, and to apply the correct substitutions as appropriate, if available. It should be a BCP 47 language code. Requires **libraqm**.
    | **embedded_color** - Whether to use font embedded color glyphs (COLR, CBDT, SBIX).


| The code below prints the text length for "Shapes" in Segoeui font at 24 point.

.. code-block:: python

    from PIL import Image, ImageDraw, ImageFont

    fnt = ImageFont.truetype("C:/Windows/Fonts/Segoeui.ttf", 24)
    with Image.open("test_images/shapes.jpg") as im:
        drw = ImageDraw.Draw(im)
        txt = "Shapes"
        textlength = drw.textbbox(xy, txt, font=fnt)
        print(textlength)


