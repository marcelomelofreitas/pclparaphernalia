# PCL Paraphernalia [![Build status](https://ci.appveyor.com/api/projects/status/qa5bqc2ji857929t/branch/master?svg=true)](https://ci.appveyor.com/project/michaelknigge/pclparaphernalia)
**PCL Paraphernalia** is a free utility which provides a small collection of tools of use to technicians supporting printing on **PCL5** (hereafter referred to as **PCL**) and **PCL6** (hereafter referred to as **PCL XL**) printers.

# Author
PCL Paraphernalia was originally written and released by Chris Hutchinson, well known 
on [TEK-TIPS.COM](https://www.tek-tips.com)
and [HP Support Community](https://h30434.www3.hp.com/t5/Meet-the-Experts/dansdaduk/ba-p/5451499) as **DansDadUK**. 

In June 2018, [Chris passed away](https://h30434.www3.hp.com/t5/LaserJet-Printing/DansDadUK/m-p/6853128#M354567) after he lost his fight with cancer. There is no comparable tool like PCL Paraphernalia
so I've created this GitHub project to make sure that his legacy will still be available to the community.

# Dependencies
The application requires the [.NET 4.x runtime](https://www.microsoft.com/en-us/download/details.aspx?id=17718) package. You need to install it separately if you are using Windows 7 or older.

# Releases
The releases here are all built by the free CI service [AppVeyor](https://www.appveyor.com/) and can be downloaded from the [Releases](https://github.com/michaelknigge/pclparaphernalia/releases). The provided installer is created with [InnoSetup](http://www.jrsoftware.org/isinfo.php).

# PCL Paraphernalia Tools
Unless otherwise stated, the tools work with **PCL** and **PCL XL**.

## Font Sample
This tool will generate a print job (**PCL** or **PCL XL**) which will print a 'font grid' showing characters from a selected **symbol set**, using a selected **font** (which may be a **printer-resident font** or a **downloadable soft font**).

When considering **downloadable soft fonts**, a side effect is that the font characteristic data (**PCL** or **PCL XL** as appropriate) will be extracted from the selected font file and displayed within the dialogue.
	
## Form Sample
This tool will generate a print job (**PCL** or **PCL XL**) which will print a specified number of pages of (preset) variable data, using the contents of one or two nominated files as **PCL macros** or **PCL XL user-defined streams** (as appropriate) to be added to the front and/or rear faces of each sheet.

## Image Bitmap
This tool will generate a print job (**PCL** or **PCL XL**) which will print a bitmap image contained in a selected bitmap file.

Note that the tool is **not** intended to be a full-blown image converter; as such, it only supports common formats (Windows v3 bitmap files of type BM, which are uncompressed, and which contain 'bottom-up' images, of 1-, 4- or 24-bits-per-pixel).

## Make Overlay
This tool parses a specified **PCL** or **PCL XL** print file, and uses this to generate a **PCL macro** or **PCL XL user defined stream** (as appropriate).

Note that this tool does not interact directly with a printer - it generates an overlay file; the generated file can be tested using the Form Sample tool.

## Misc Samples
This tool provides simple examples of **PCL** or **PCL XL** usage of:

 - colour
 - logical operations
 - logical page definition
 - patterns
 - text modification
 - Unicode characters

## Print Area
This tool will generate a print job (**PCL** or **PCL XL**) which will print a page indicating the printable area available for the selected page **size** and **orientation**.

## Print Languages
This tool displays lists of the language elements (escape sequences, commands, tags, etc.) associated with the common Page Description Languages (PDLs) and Job Control languages used on modern PCL printers.

Details are provided for **PCL**, **PCL XL**, **HP-GL/2**, **PJL** and **PML**.

Note that this tool does not interact with a printer - it merely displays details from built-in tables.

## PRN File Analyse
This tool provides an analysis of the contents of a nominated print file.

It recognises and deciphers **PCL**, **PCL XL**, **HP-GL/2**, **PJL** and **PML**.

Note that this tool does not interact with a printer - it analyses a nominated file.

## PRN File Print
This tool sends the contents of a nominated print file to the target printer.

The contents of the file must be compatible with the capabilities of the printer: for example, there is no point in sending a PCL print file to a printer which does not understand PCL.

## Soft Font Generate
This tool will generate a **PCLETTO** (**PCL**  **E**ncapsulated **T**rue**T**ype **O**utline) soft font (**PCL** or **PCL XL**), bound to a specified **symbol set**, from a donor **TrueType** font.

Note that this tool does not interact directly with a printer - it generates a soft font file; the generated file can be tested using the Font Sample tool.

## Status Readback
This tool sends a request for information to the target printer, then reads and displays the response.

There are two main types of information: **PCL** or **PJL** status requests; each type is divided into sub-types.

## Symbol Set Generate
This tool provides a means to define a **PCL** symbol set; the definition is stored in a file which can subsequently be downloaded to a target printer, or (via the Soft Font Generate tool) used in the construction of a soft font **bound** to this symbol set.

## Tray Map
This tool will generate a print job (**PCL** or **PCL XL**) which contains one or more pages, each selecting a paper tray using a combination of one or more of **paper size**, **paper type**, and **tray identifier**.
