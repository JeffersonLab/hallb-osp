Hall B Operation Manual & ESAD Information
===========================================

14 May 2014

The ESAD Introduction (Chapter1) and General Hazards (Chapter2) are located at:

src/esad

The rest of the ESAD materials are pulled directly from the operations manual
either as level zero, safety, or uncommented information.

-
Stored at  github dir -----.   

The  document is being generated using the Hall A teplate created by E. Chudakov  from March 2014.

This document is intended to provide guidelines for Scientists (both staff and visitors) how to
safely operate the standard equipment in Hall B.

This document is NOT intended to provide guidelines for technical equipment (such as manlifts or the crane) 
that require special training to operate NOR does the document provide guidelines on how do electrical work.   An example of what should be covered is how to safely reset the 
power supplies (i.e. something that a scientist has
done in the past).


For the high level outline, the name next to the section is just the led person for that part and is not 
expected to be the sole person working on that section.   In general, you should be working on the same 
sections you worked on in 2011.

High Level OUTLINE

I. Hall B Safety Document Overview [V.B.]

II. Beamline Equipment [F.-X. G.]

III. Target and Magnet Controls [D.T.] 

IV. Tracking Detectors and TOF  [Y.G, D.C. and M.M.]

V.  PID Detectors (shower and  Cherenkov Detectors) [S.S. and Y.S.]

VI. Slow Controls [K.L.]

VII. DAQ [S.B.]


VIII. Offline Software [V.Z.]

IX. HPS [S.S.]

-

To update the document, clone the github directory and recompile the latex 
(if you know what section you editted last time, likely you just need to do it again adding a checklist)

http://github.com/JeffersonLab/hallb-osp/

All materials should be in LaTeX, images preferably in eps.

For unix/linux users; you can quickly pull a copy of the current materials by typing into a comment line:

git clone https://github.com/JeffersonLab/hallb-osp.git

I would encourage anyone who knows git or who is want to learn git to setup a github account.   I just need to know your github your name so you can be added to the offical Jefferson Lab 

LaTeX Information
-----------------

The purpose of this package is to produce the Hall B OSP manual
in PDF and HTML formats. It contains the source of the text, 
the pictures and tools to make the documents. 

Top directory, static:
src/ - the source (LaTeX) and pictures
scripts/ - auxiliary scripts and the makefile
misc/ - miscellaneous documents - not used regularly

Top directory, dynamic:
run/ - work directory to create the documents

One can create the OSP document with different levels of
detail (noted as "infolevel"), the lower the value, 
the more slim is the document. All the levels contain the 
basic safety information for every system. Additional 
information depends on the level:
infolevel=0 - a short (1 page) description per system including 
              a picture for the layout if needed;
infolevel=1 - plus a description of the system's components;
infolevel=2 - plus a description of the procedures and pictures, 
              like MEDM windows in PNG format;  
infolevel=3 - plus the main principles of the devices' operation;
infolevel=4 - plus photographs and other large pictures
 
Producing the Documents:
-----------------------
In order to produce the OSP document with, say, infolevel=4 one 
has to:
1) ./scripts/config osp 4   (in the top directory)
   This creates a work directory run/ to produce the document 
2) cd run/
3) make pdf  - to create the document (osp.pdf) in PDF format 
4) make html - to create the document (in osp_html/) in HTML format

Browsing the PDF document: 
-------------------------
The PDF can be viewed with Acrobat Reader or xpdf (on Linux).
Both browsers can search for a given word. Also, the 
document contains hyper-references both inside the document
(so, one can jump forth and back to, say, the literature 
references), and also outside, using the standard URL.
In order to use the external references one may need 
to configure the browsers. Use the "Edit/Preference" button
on acroread. For xpdf you may need to copy /etc/xpdfrc
to ~/.xpdfrc and edit it, uncommenting the line
#urlCommand     "netscape -remote 'openURL(%s)'"
and commenting out the previous line.
Typically, xpdf/acroread tries to use an existing WWW browser
window and does not open a new window.

