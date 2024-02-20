{
  "date": "2021-03-08",
  "keywords": [
    "PML",
    "eReader",
    "extension",
    "format",
    "eBook",
    "Palm Markup Language"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about PML file format, Palm Markup Language and APIs that can create and open PML files.",
  "title": "PML - Palm Markup Language File",
  "linktitle": "PML",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml"
    }
  },
  "lastmod": "2021-03-08"
}

## What is a PML file?

Palm Inc introduced the PML file format which stands for Palm Markup Language File. Its purpose is to create docs for eReader which is an eBook reading device similar to the tablet computer. The PML file gives the layout to a [PDB](/programming/pdb/) file (containing various data files) to display on a Palm Device.

## Technical details of PML Files

The structure of PML files consists of tags for creating an eBook setup, including paragraphs, headings, indentations, and references. It also allows the formatting tags such as Bold, Small Caps, and Superscript. Developers can also add images to the eBooks.

### Palm Markup Language
The following table specifies the PML commands:

|Command|Description|
---|---|
|             \p              |                                                                                                                              New page                                                                                                                               |
|             \x              |                                                                                New chapter; also causes a new page break. Enclose chapter title (and any style codes) with \x and \x                                                                                |
|             \Xn             |                                            New chapter, indented n levels (n between 0 and 4 inclusive) in the Chapter dialog; doesn't cause a page break. Enclose chapter title (and any style codes) with \Xn and \Xn                                             |
|     \Cn="Chapter title"     | Insert "Chapter title" into the chapter listing, with level n (like \Xn). The text is not shown on the page and does not force a page break. This can sometimes be useful to insert a chapter mark at the beginning of an introduction to the chapter, for example. |
|             \c              |                                                                                                    Center this block of text; close with \c on beginning of line                                                                                                    |
|             \r              |                                                                                                    Right justify text block; close with \r on beginning of line                                                                                                     |
|             \i              |                                                                                                                   Italicize block; close with \i                                                                                                                    |
|             \u              |                                                                                                                   Underline block; close with \u                                                                                                                    |
|             \o              |                                                                                                                   Overstrike block; close with \o                                                                                                                   |
|             \v              |                                                                                                      Invisible text; close with \v (can be used for comments)                                                                                                       |
|             \t              |                                                                                             Indent block. Start at beginning of a line, close with \t at end of a line                                                                                              |
|          \T="50%"           |                                             Indents the specified percentage of the screen width, 50% in this case. If the current drawing position is already past the specified screen location, this tag is ignored.                                             |
|          \w="50%"           |                                     Embed a horizontal rule of a given percentage width of the screen, in this case 50%. This tag causes a line break before and after it. The rule is centered. The percent sign is mandatory.                                     |
|             \n              |                                                                                                     Switch to the "normal" font, which is specified by the user                                                                                                     |
|             \s              |                                                                                                      Switch to stdFont; close with \s to revert to normal font                                                                                                      |
|             \b              |                                                                                       Switch to boldFont; close with \b to revert to normal font (deprecated; use \B instead)                                                                                       |
|             \l              |                                                                                                     Switch to largeFont; close with \l to revert to normal font                                                                                                     |
|             \B              |                                                          Mark text as bold. Unlike the \b tag, \B doesn't change the font, so you can have large bold text. You cannot mix \b and \B in the same PML file.                                                          |
|             \Sp             |                                                                   Mark text as superscript. Should not be mixed with other styles such as bold, italic, etc. Enclose superscripted text with \Sp.                                                                   |
|             \Sb             |                                                                     Mark text as subscript. Should not be mixed with other styles such as bold, italic, etc. Enclose subscripted text with \Sb.                                                                     |
|             \k              |                        Make enclosed text into small-caps; close with \k. Any characters enclosed in \k tags (including those with accents) are made uppercase and are rendered at a smaller point size than a regular uppercase character.                         |
|             \\              |                                                                                                                    Represents a single backslash                                                                                                                    |
|            \aXXX            |                                                                             Insert non-ASCII character whose Windows-1252 code is decimal XXX. See the PML character table for details.                                                                             |
|           \UXXXX            |                                                                        Insert non-ASCII character whose Unicode code is hexadecimal XXXX. See the Extended PML character table for details.                                                                         |
|     \m="imagename.png"      |                                                                                                      Insert the named image. See the section on Images below.                                                                                                       |
| \q="#linkanchor"Some text\q |                           Reference a link anchor which is at another spot in the document. The string after the anchor specification and before the trailing \q is underlined or otherwise shown to be a link when viewing the document.                           |
|       \Q="linkanchor"       |                                                                                                               Specify a link anchor in the document.                                                                                                                |
|             \-              |                                                                                 Insert a soft hyphen. A soft hyphen shows up only if it is necessary to break a word across a line.                                                                                 |
|     \Fn="footnote1"1\Fn     |                                                             Link the "1" to a footnote whose name is footnote1, tagged at the end of the PML document. See the section on Footnotes and Sidebars below.                                                             |
|  \Sd="sidebar1"Sidebar\Sd   |                                                        Link the "Sidebar" text to a sidebar whose name is sidebar1, tagged at the end of the PML document. See the section on Footnotes and Sidebars below.                                                         |
|             \I              |                                                              Mark as a reference index item. Enclose index item (and any style codes) with \I and \I.|                                                           
 

## References

* [Palm Markup Language - By MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)
