Thumbnailer
===========

This is a Java Plugin for creating Thumbnails of files during the crawling process of regain.<br>
(Regain is a Lucene-based desktop search engine.)

*Status* : Beta (Functional)<br>
*Licence* : GNU GPL 2.1 or later

Roadmap
-------

* Creation of Thumbnails *(DONE 14.06.2011)*
* Add capability for Crawling Plugins to regain *(DONE 29.07.2011)*
* Integration into regain (as a Plugin) *(DONE 29.07.2011)*
* Packaging in .jars / dynamic loading of .jars *(DONE 29.07.2011)*
* Seperation from regain lib-wise (so that it can be used as stand-alone/library) *(DONE 28.07.2011)*
* Show Thumbnails in results if available
  * Create Thumbnail-Tag


Supported Fileformats
---------------------

* Office files (doc, docx, xls, xlsx, ppt, pptx)
* OpenOffice files (all of them)
* Text files (txt, pdf, rtf)
* Image files (jpg, png, bmp, gif, tiff?)
* MIT Scratch files (sb)

(Detection is based on MIME-Type, not filename extension. So files with an incorrect file extension will be treated correctly, not as they deserve.) 

TODO
----

### Thumbnailer:
* Migrate to JODConverter 3beta (reduce hassle of start/stop/document timeout) (DONE)
  * remove log4j info messages
  * Upgrade to 3beta4 when it appears
  * Find a way to let him fail if he can't convert the file (sb is a binary format and really shouldn't be treated as plain text.)
* PDFBox: Library Conflict with regain. (We need to include this in the plugin, but it is included in a maybe-loaded preparator as well.)
  * That means that both should be updated at the same time! (1.6.0 is already out.)
* Check that all temporary files are deleted during thumbnailing process

### Bugs:

### Test: 

* MacOS hasn't been tested yet
* MIME Tests aren't correctly working yet

### Nice-to-have:

* .tiff-Support (via ImageMagick?)
* IFilterThumbnailer for Windows
* JMF / ffmpeg for video thumbnailing
* Run optipng on all pngs (via cron)
* Better performance for PDFBox

Author
------

This is a project of the university of Siegen for the benefit of [come_IN Computerclubs](http://www.computerclub-comein.de). But of course, if you have patches etc. go ahead!
