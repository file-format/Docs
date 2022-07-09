{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XPI - Cross-platform Installer Package File",
  "description":"Learn about XPI file format and APIs that can create and open XPI files.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-06-07"
}

## What is an XPI file?

An XPI file is an installation archive that is compressed to reduce the size of the file. It is used by Mozilla applications for installation of plugins and add-on files. It contains an installation script or a manifest at the root of the file along with a number of data files.  An XPI file may contain themes, toolkit, or Firefox plugins that user can install to become part of the Firefox browser, Thunderbird or SeaMonkey.

## XPI File Format - More Information

XPI files are saved to disc as [ZIP](/compression/zip/) archives that combine multiple files into a single compressed file. The files inside an XPI file may include installation script file such as JS and web files such as [CSS](/web/css/), [HTML](/web/html/) and [JSON](/web/json/). Sometimes, it may also contain [PNG](/image/png/) image files to be used as icons by add-on.

### How to view XPI file's contents?

An XPI file is practically a ZIP archive whose contents can be viewed using the following steps.

 * Change the extension of file from XPI to ZIP
 * Extract the contents of the file using any standard decompression utility such as WinZip (Windows, Mac), 7-Zip (Windows), or Apple Archive Utility (Mac).

### Install XPI File on Firefox Android

Mostly people are curious to know if XPI files can be installed in Firefox on Android devices. On Android, you can install add-on from an XPI file by locating the file and opening it with Firefox.

## References

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [How can I open an XPI File Extension?](https://support.mozilla.org/en-US/questions/1009049)
