=====================================
256colors - ANSI colorcode calculator
=====================================

:Author: Jakob westhoff
:Revision: Draft
:Date: 2011-06-17


About
=====

Modern terminal emulators are capable of displaying a lot more than the 16
usual colors. In fact most currently used terminals can display up to 256
different colors.

256colors is a bash script, which is capable of outputting a nicely formatted
table of all available colors as well as calculating the nearest match for
a given RGB color.


Usage
=====

The ``256colors.sh`` script does support two different modes of operation::

    Usage: ./256colors.sh <action> [options ...]

    Actions:

      grid [colors per row] [skipped start colors]

        Print a grid of all terminal colors in the given format.
        A line break is printed after the given amount of colors has been outputted.
        An arbitrary amount of colors may be skipped at the start of the table.
        Both arguments are optional. By default 6 colors per line are printed, while
        the first 16 colors are skipped

      calculate <r> <g> <b>
        
        Calculate the best match for the given rgb color (0-255)


grid
----

The grid operation does output a nicely formatted table of all available color
codes inside your current terminal emulation.

.. image:: https://github.com/jakobwesthoff/256colors/raw/master/screenshots/grid.png
   :alt: Grid operation of 256colors in action
   :align: center


calculate
---------

The calculate operation tries to find the nearest possible matching colorcode
for a given RGB color value. The color has to be provided as a tuple of three
values ranging from ``0-255``, each of them providing information about one
color channel.

.. image:: https://github.com/jakobwesthoff/256colors/raw/master/screenshots/calculate.png
   :alt: Calculate operation of 256colors in action
   :align: center
