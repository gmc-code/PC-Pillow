==========================
ImageDraw textbbox
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageDraw.html#PIL.ImageDraw.ImageDraw.textbbox
| See: https://pillow.readthedocs.io/en/stable/handbook/text-anchors.html#text-anchors

----

Draw
Rectangle
----------------------

| Use the ``ImageDraw.textbbox(xy, text, font=None, anchor=None, spacing=4, align='left', direction=None, features=None, language=None, stroke_width=0, embedded_color=False)`` method to return the bounding box (left, top, right, bottom, in pixels) of given text relative to q given anchor when rendered in TrueType font.

.. py:function:: ImageDraw.textbbox(xy, text, font=None, anchor=None, spacing=4, align='left', direction=None, features=None, language=None, stroke_width=0, embedded_color=False)

    | **xy** - The anchor coordinates of the text.
    | **text** - Text to be measured. If it contains any newline characters, the text is passed on to ImageDraw.multiline_textbbox`.
    | **font** - A ImageFont.FreeTypeFont instance such as ``ImageFont.truetype("C:/Windows/Fonts/Segoeui.ttf", 24)``
    | **anchor** - The text anchor alignment. Determines the relative location of the anchor to the text. The default alignment is ``la`` for left ascender, top left.
    | **spacing** - If the text is passed on to ImageDraw.multiline_textbbox, the number of pixels between lines.
    | **align** - If the text is passed on to ImageDraw.multiline_textbbox`, ``"left"``, ``"center"`` or ``"right"``. Determines the relative alignment of lines.
    | **direction** - Direction of the text. It can be ``"rtl"`` (right to left), ``"ltr"`` (left to right) or ``"ttb"`` (top to bottom). Requires **libraqm**.
    | **features** - A list of OpenType font features to be used during text layout. This is usually used to turn on optional font features that are not enabled by default, for example ``"dlig"`` or ``"ss01"``, but can be also used to turn off default font features, for example ``"-liga"`` to disable ligatures or ``"-kern"`` to disable kerning. Requires **libraqm**.
    | **language** - Language of the text. Different languages may use different glyph shapes or ligatures. This parameter tells the font which language the text is in, and to apply the correct substitutions as appropriate, if available. It should be a BCP 47 language code. Requires **libraqm**.
    | **stroke_width** - The width of the text stroke.
    | **embedded_color** - Whether to use font embedded color glyphs (COLR, CBDT, SBIX).


| The code below prints the text length for "Shapes" in Segoeui font at 24 point.

.. code-block:: python

    from PIL import Image, ImageDraw, ImageFont

    fnt = ImageFont.truetype("C:/Windows/Fonts/Segoeui.ttf", 24)
    with Image.open("test_images/shapes.jpg") as im:
        drw = ImageDraw.Draw(im)
        txt = "Shapes"
        textbbox_val = drw.textbbox((0,0), txt, font=fnt)
        print(textbbox_val)


