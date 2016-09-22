root2html
=============

A script that generates html and images from a ROOT file of TCanvases.

authors:

-   Ryan Reece <ryan.reece@cern.ch>
-   Tae Min Hong <tae.min.hong@cern.ch>
-   Alex Tuna <tuna@cern.ch>

created: February 16, 2011


Description
----------------------------------

root2html is a script for generating an html page for displaying plots.
root2html expects you to pass a root file, filled with TCanvases,
possibly organized in TDirectories.  The canvases presumably have plots
that you have pre-made and styled however you like.  root2html inspects
the root file and walks its directories.  Then, for each canvas, it
inspects  all objects that have been drawn to the canvas, and gets
statistics depending on the object's type.  These stats are displayed in
the caption when you click on a figure.  Then, root2html creates eps and
gif/png images for each of the plots, and generates an html page
containing and linking all the information.

When viewing the output html, note that you can click-up more than one
figure at a time, and drag them around the screen.  That javascript magic
is done with the help of this library: <http://highslide.com/>.


Installation
----------------------------------

Assuming you have a working ROOT installation with PyROOT, the only other
requirement is that you download the highslide javascript library at
<http://highslide.com/>, unzip it, and set the highslide_path variable to
point to the path: highslide-(version)/highslide (see the `root2html.py` file).


Options
----------------------------------

    -h, --help
        Prints this manual and exits.
    -p PATTERN, --pattern=PATTERN
        Regex pattern for filtering the TCanvas paths processed.  The pattern
        is matched against the full paths of the TCanvases in the root file.
    -j PATH, --highslide=PATH
        Overrides the default path to highslide.


License
----------------------------------

-   Copyright 2011-2015 The authors
-   License: GPL <http://www.gnu.org/licenses/gpl.html>


