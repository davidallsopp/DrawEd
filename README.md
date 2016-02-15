
#DrawEd

##Help for Version 2.42 : (17 Jan 2000)

------

DrawEd is a simple multitasking application for the processing of Drawfiles
in ways not possible using Draw or DrawPlus 

#FEATURES:

* Search-and-Replace of colours
* Lightening and Darkening by any amount
* Conversion of colour to greyscale 
* Conversion of colour to monochrome with adjustable threshold
* Inversion of colours

* Can operate seperately on lines, fills and text.

#USE OF DRAWED:

Click on the icon-bar icon to open the DrawEd window.

Set the options you require (detailed below) and drag your drawfile into the
window or onto the icon-bar. A Save window will open - drag the save icon to
a directory to save the processed file.

You can apply more than one process to your file by selecting the extra
processes using ADJUST. Note that the processes will be carried out in the
order that they appear in the window. If you want to use the processes in
a different order then use the Reprocess facility. (see below)

DrawEd is intended to be used alongside Draw or DrawPlus; these
applications should be used for viewing the results.

#SEND TO DRAW:

If "Send to Draw" is ticked in the icon bar menu, DrawEd will load the
processed file automatically into Draw or DrawPlus if they are running.

#REPROCESS

DrawEd works by making a copy of your original file, then changing this
copy. Once you have made one change to your file, you can click REPROCESS to
make further changes - just set the options and click REPROCESS.

#OPTIONS

##SEARCH & REPLACE  

This option simply searches for a colour in the original file and replaces
it with a new one. Enter the R G B values of the colour to search for, and
the values for the one to replace it. You may need to use Draw to find out
the values in the original file or to see what particular values look like.

You can specify "No Colour" (ie transparent) by clicking the NONE icon.

You can search for only lines, or fills, or text of a particular colour, or
any combination of these. DrawEd will give a warning if you don't have any
of these set when you try to process a file.

##LIGHTEN , DARKEN

Pretty obvious really! The Lighten option is particularly useful for
printing out files, which come out too dark with some printers. For clip
art it is often useful to leave outlines black, and just lighten the fills.
You will have to experiment with your printer for the ideal lightening value - try 20-40% to start with. 

Very high values of Lighten or Darken will obviously leave you with an
almost completely white or black image.

##256 GREYSCALE

This simply converts a colour file to a greyscale file. Colour Correction
may be used - this attempts to compensate for the apparently different
brightness of different colours, so that the grey image looks more true to
the original colour image. The greyscale option can be used to predict what a
colour file will look like when printed in monochrome. 

##MONO 

This converts a colour (or greyscale) file to black and white, and can
sometimes make an image more striking - try it and see. Altering
the Threshold value determines how bright something has to be to be made
white rather than black.  (A high value turns most things black, a low value
turns most things white)  Colour correction may be used.

##INVERT

This reverses the R G B components of colours. The effect on a colour file
will usually be interesting, but not very useful. Inverting monochrome
clipart can give useful inverse images - Using a 'positive' and a 'negative'
image can look good in a design.

----------------------------------------------------------------------------

#Notes:

1. Text in Draw can have a 'background' colour setting, which is used to
determine what colours to use for antialiasing. If you alter the text colour
or the colour of objects behind the text then the antialiasing may look
odd on screen, as DrawEd doesn't alter the background setting to match.
The file will print normally.
2. This version of DrawEd does not operate on Text Areas, because the
colours are stored in a different way to other objects.

----------------------------------------------------------------------------

#Changes

Changes from version 2.41 (12/7/96!!) - Force first byte of colour to be zero
rather than assuming it to be so.  According to the drawfile spec I have, this
byte should be zero, reserved for future expansion. However, someone has sent me
a drawfile with the same version number in which this byte is non-zero; hence
the change to cope with these files.

Committed to github in Feb 2016 from an ancient backup. The main !RunImage file seems to be a tokenized BBC BASIC file, not a text file, so is not friendly to modern editors - nor can I verify that the code still works. If anyone is interested and can get it working on a RiscPC or Raspberry Pi, then I'd be interested in a plain text version!

Matt Godbolt's detokenizer at http://xania.org/200711/bbc-basic-v-format seems to be able to read and convert the !RunImage (many thanks!), though I can't currently verify the output is 100% correct!

Also added Apache License. This supersedes any original license conditions in the !Help file.

