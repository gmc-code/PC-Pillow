==========================
ImageColor getcolor
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageColor.html#PIL.ImageColor.getcolor

----

getcolor
---------------------------

| The function, ``ImageColor.getcolor(color, mode)``, takes a color string and returns a greyscale value.

.. py:function:: ImageColor.getcolor(color, mode)

    | **color** is a color which may include standard html color names strings and hex colour strings.
    | **mode** is "L" for greyscale.
    | e.g. "red", (255, 0, 0) returns 76 

----

Examples
----------------

| The function, ``get_rgb_colors``, passes in a list of colours and returns a list of rgb tuples.
| The function, ``get_color_colors``, passes in a list of colours and returns a list of greyscale values.

.. code-block:: python

    from PIL import Image, ImageColor

    def get_color_colors(colors):
        colors_g = [ImageColor.getcolor(color, mode="L") for color in colors]
        return colors_g

    colors = ["red", "green", "blue", "yellow"]
    print(get_color_colors(colors))
    # [76, 75, 29, 226]

    colors = ["rgb(255, 0, 0)", "rgb(0, 128, 0)"]
    print(get_color_colors(colors))
    # [76, 75]

    colors = ["rgb(100%, 0%, 0%)", "rgb(0%, 50%, 0%)"]
    print(get_color_colors(colors))
    # [76, 75]

    colors = ["#ff00ff", "#00ffff", "#ffff00"]
    print(get_color_colors(colors))
    # [105, 179, 226]

    colors = ["hsv(120,100%,100%)", "hsv(120,100%,50%)", "hsv(120,50%,100%)"]
    print(get_color_colors(colors))
    # [150, 75, 203]

    # with transparency
    colors = ["#ff0000ff", "#ff0000cc", "#ff000080"]
    print(get_color_colors(colors))
    # [76, 76, 76]
