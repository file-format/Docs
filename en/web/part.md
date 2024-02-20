{
  "date": "2021-06-24",
  "keywords": [
    "PART",
    "partial",
    "extension",
    "file",
    "format",
    "web",
    "downloaded"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "PART - Partially Downloaded File",
  "description": "Learn about PART file format and APIs that can create and open PART files.",
  "linktitle": "PART",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-part"
    }
  },
  "lastmod": "2021-06-24"
}

## What is a PART file? ##

A part file or .part extension is a partially downloaded file. It is used when downloads are in progress or have been interrupted due to any issue, giving the download manager an opportunity to resume the download whenever possible. 
This means that the browser, such as Firefox or file transfer programs like eMule, eMule plus, FlashGet, etc. stores a portion of the file, called Part file, while the downloading is occurring on your device. This part file will show you if the download is in progress or has been interrupted before completion. Not only this but the PART file stores all the data till the download is completed which is why some of them can later be resumed if you want to start the download again.

## PART File Format ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.