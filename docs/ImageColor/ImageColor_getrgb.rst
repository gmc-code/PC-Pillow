==========================
ImageColor getrgb
==========================

| See: https://pillow.readthedocs.io/en/stable/reference/ImageColor.html#PIL.ImageColor.getrgb
| See: https://htmlcolorcodes.com/color-names/

----

getrgb
---------------------------

| The function, ``ImageColor.getrgb(color)``, takes a color string and returns an rgb tuple.

| The getrgb syntax is: 

.. py:function:: ImageColor.getrgb(color)

    | **color** is a color which may include standard html color names strings and hex colour strings.
    | e.g. "red" is converted to (255, 0, 0)
    | e.g. "#ffccff" is converted to (255, 204, 255)

----

Examples
----------------

| The function, ``get_rgb_colors``, passes in a list of colours and returns a list of rgb tuples.
| The function, ``get_color_colors``, passes in a list of colours and returns a list of greyscale values.

.. code-block:: python

    from PIL import Image, ImageColor


    def get_rgb_colors(colors):
        colors_rgb = [ImageColor.getrgb(color) for color in colors]
        return colors_rgb

    def get_color_colors(colors):
        colors_g = [ImageColor.getcolor(color, mode="L") for color in colors]
        return colors_g

    colors = ["red", "green", "blue", "yellow"]
    print(get_rgb_colors(colors))
    # [(255, 0, 0), (0, 128, 0), (0, 0, 255), (255, 255, 0)]
    print(get_color_colors(colors))
    # [76, 75, 29, 226]

    colors = ["rgb(255, 0, 0)", "rgb(0, 128, 0)"]
    print(get_rgb_colors(colors))
    # [(255, 0, 0), (0, 128, 0)]
    print(get_color_colors(colors))
    # [76, 75]

    colors = ["rgb(100%, 0%, 0%)", "rgb(0%, 50%, 0%)"]
    print(get_rgb_colors(colors))
    # [(255, 0, 0), (0, 128, 0)]
    print(get_color_colors(colors))
    # [76, 75]

    colors = ["#ff00ff", "#00ffff", "#ffff00"]
    print(get_rgb_colors(colors))
    # [(255, 0, 255), (0, 255, 255), (255, 255, 0)]
    print(get_color_colors(colors))
    # [105, 179, 226]

    colors = ["hsv(120,100%,100%)", "hsv(120,100%,50%)", "hsv(120,50%,100%)"]
    print(get_rgb_colors(colors))
    # [(0, 255, 0), (0, 128, 0), (128, 255, 128)]
    print(get_color_colors(colors))
    # [150, 75, 203]

    # with transparency
    colors = ["#ff0000ff", "#ff0000cc", "#ff000080"]
    print(get_rgb_colors(colors))
    # [(255, 0, 0, 255), (255, 0, 0, 204), (255, 0, 0, 128)]
    print(get_color_colors(colors))
    # [76, 76, 76]
