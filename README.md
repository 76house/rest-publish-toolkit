rest-publish-toolkit
====================

Scripts and templates for easy publishing of technical documentation or other documents written in reSructuredText. Tested in Ubuntu 12.10 so far.

Prerequisities
--------------

- Install python with setuptools, rst2pdf, pdftk and calibre
- Install the following python packages via easy_install: docutils, reportlab, wordaxe

Usage
-----

- Have a look at ``template.rst`` and included ``*.rst`` files. It is a template for creating technical documentation, however feel free to adjust it to your needs. Also check out the [syntax reference](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html)
- Edit the document information in ``metadata.txt``
- Replace ``somepassword`` in ``./generate`` script to keep the PDF output secure
- Optionally, change the cover backgrounds ``manual-cover-front.pdf`` and ``manual-cover-back.pdf`` (the source SVGs are placed in ``images`` subdirectory)
- Run the conversions with ``./generate`` script

Output
------

The ``./generate`` script creates the following files in ``output`` subdirectory:

- **PDF document**, with embedded fonts and basic encryption
- **HTML document** with embedded stylesheet and images placed in ``output/images`` subdirectory
- **EPUB ebook** with embedded stylesheet and cover image
- **MOBI ebook for Kindle** with embedded stylesheet and cover image

