rest-publish-toolkit
====================

Scripts and templates for easy publishing of technical documentation or other documents written in reSructuredText. The same source is used for print (PDF), online (HTML) and ebook output (EPUB, MOBI).

Tested in Ubuntu 12.10 so far.

Prerequisities
--------------

- Install rst2pdf, pdftk and calibre and python with setuptools
- Install the following python packages via easy_install: docutils, reportlab, wordaxe
- Install [Droid fonts](http://www.droidfonts.com/droidfonts/)

Usage
-----

- Have a look at ``template.rst`` and included ``*.rst`` files. It is a template for creating technical documentation, however feel free to adjust it to your needs. Also check out the [syntax reference](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html)
- Edit the document information in ``metadata.txt``
- Replace ``somepassword`` in ``./generate`` script to keep the PDF output secure
- Optionally, set replace Droid fonts in ``template.sheet`` and ``template.css`` with your favorite fonts
- Optionally, change the cover backgrounds ``manual-cover-front.pdf`` and ``manual-cover-back.pdf`` (the source SVGs are placed in ``images`` subdirectory)
- Run the conversions with ``./generate`` script

Output
------

The ``./generate`` script creates the following files in ``output`` subdirectory:

- **PDF document**, with embedded fonts and basic encryption
- **HTML document** with embedded stylesheet and images placed in ``output/images`` subdirectory
- **EPUB ebook** with embedded stylesheet and cover image
- **MOBI ebook for Kindle** with embedded stylesheet and cover image

Notes
-----

The reST markup processing with ``rst2pdf`` may be a bit tricky sometimes. Refer to [rst2pdf group](https://groups.google.com/forum/?fromgroups#!forum/rst2pdf-discuss) for further info.
