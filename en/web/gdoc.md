{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GDOC File - Google Docs Shortcut",
  "description": "Learn about what is a GDOC file and APIs that can create and open GDOC files.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdoc"
    }
  },
  "lastmod": "2022-01-23"
}

## What is a GDOC file?

A GDOC file is a shortcut file that points to a file located on Google Drive, a cloud-based document storage service. When Google Drive client is installed on a computer and a document is created inside it, the drive creates a document in the online cloud storage and writes the [URL](/web/url/) of this document in the GDOC file in local Google Drive folder. When this shortcut file is double clicked, the default web browser opens the document from the [URL](/web/url/) location. If this shortcut file is moved out of this folder, the link to online document is broken.

## GDOC File Format - More Information

GDOC file contains shortcut to the online document written in [JSON](/web/json/) file format. The browser opening GDOC files read the URL information and opens the linked document for display provided the user is logged in to this Google account where the document is stored. GDOC files doesn't contain the contents of the document.

### GDOC File Example

GDOC file can be opened in a text editor and its contents looks like following.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

As can be seen, the contents are formatted in JSON having a document's URL and the associated document ID.

## References

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)
