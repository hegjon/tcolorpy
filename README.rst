.. contents:: **tcolorpy**
   :backlinks: top
   :depth: 2


Summary
============================================
tcolopy is a Python library to apply true color for terminal text.

.. image:: https://badge.fury.io/py/tcolorpy.svg
    :target: https://badge.fury.io/py/tcolorpy
    :alt: PyPI package version

.. image:: https://anaconda.org/conda-forge/tcolorpy/badges/version.svg
    :target: https://anaconda.org/conda-forge/tcolorpy
    :alt: conda-forge package version

.. image:: https://img.shields.io/pypi/pyversions/tcolorpy.svg
    :target: https://pypi.org/project/tcolorpy
    :alt: Supported Python versions

.. image:: https://img.shields.io/pypi/implementation/tcolorpy.svg
    :target: https://pypi.org/project/tcolorpy
    :alt: Supported Python implementations

.. image:: https://github.com/thombashi/tcolorpy/workflows/Tests/badge.svg
    :target: https://github.com/thombashi/tcolorpy/actions?query=workflow%3ATests
    :alt: Linux/macOS/Windows CI status

.. image:: https://coveralls.io/repos/github/thombashi/tcolorpy/badge.svg?branch=master
    :target: https://coveralls.io/github/thombashi/tcolorpy?branch=master
    :alt: Test coverage: coveralls


Installation
============================================

Installation: pip
------------------------------
::

    pip install tcolorpy

Installation: conda
------------------------------
::

    conda install -c conda-forge tcolorpy


Usage
============================================

Library usage
--------------------------------------------

:Sample Code:
    .. code-block:: python

        from tcolorpy import tcolor

        print(tcolor("tcolopy example", color="#ee1177", styles=["bold", "italic", "underline"]))

:Output:
    .. figure:: https://cdn.jsdelivr.net/gh/thombashi/tcolorpy@master/ss/oneline.png
        :scale: 60%
        :alt: https://github.com/thombashi/tcolorpy/blob/master/ss/oneline.png

You can set the following ``tcolor`` arguments:

- ``color``/``bg_color``
    - color names (``"red"``, ``"red"``, etc.) or color code (``"#RRGGBB"``)
- ``styles``
    - ``"bold"``, ``"italic"``, etc.


Other examples
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Apply true color and styles to text:

.. figure:: https://cdn.jsdelivr.net/gh/thombashi/tcolorpy@master/ss/styles.png
    :scale: 60%
    :alt: https://github.com/thombashi/tcolorpy/blob/master/ss/styles.png

    `tcolorpy/ansi_styles.py <https://github.com/thombashi/tcolorpy/blob/master/examples/ansi_styles.py>`__

You can also specify colors by names:

.. figure:: https://cdn.jsdelivr.net/gh/thombashi/tcolorpy@master/ss/ansi_colors.png
    :scale: 60%
    :alt: https://github.com/thombashi/tcolorpy/blob/master/ss/ansi_colors.png

    `tcolorpy/ansi_colors.py <https://github.com/thombashi/tcolorpy/blob/master/examples/ansi_colors.py>`__


CLI usage
--------------------------------------------
``tcolorpy`` can be used via CLI:

::

    $ python -m tcolorpy "tcolopy example" -c "#ee1177" -s bold,italic,underline

Command help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

    usage: __main__.py [-h] [-c COLOR] [-b BG_COLOR] [-s STYLES] [--encode ENCODE]
                       string

    positional arguments:
      string                string to apply styles.

    optional arguments:
      -h, --help            show this help message and exit
      -c COLOR, --color COLOR
                            specify a color code (#XXXXXX) or a name. valid names
                            are: black, red, green, yellow, blue, magenta, cyan,
                            white, lightblack, lightred, lightgreen, lightyellow,
                            lightblue, lightmagenta, lightcyan, lightwhite
      -b BG_COLOR, --bg-color BG_COLOR
                            specify a background color code (#XXXXXX) or a name.
                            valid names are: black, red, green, yellow, blue,
                            magenta, cyan, white, lightblack, lightred,
                            lightgreen, lightyellow, lightblue, lightmagenta,
                            lightcyan, lightwhite
      -s STYLES, --styles STYLES
                            specify a comma separated styles. valid values are:
                            bold, dim, italic, underline, blink, invert, strike
      --encode ENCODE       output a text encoded with the specified encoding


Dependencies
============================================
Python 3.6+
No external dependencies.
