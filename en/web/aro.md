{
  "date" : "2021-12-09",
  "keywords" : [ "aro",".aro file", "aro file format", "an file type", "file", "type", "what is a .aro file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ARO File Format - SteelArrow Web Application File",
  "description" : "Learn about what is an ARO file and APIs that can create and open ARO files.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-12-09"
}

## What is an ARO file?

An ARO file is a server side web page file that is generated with SteelArrow Web Application. It contains [HTML](/web/html/) and SteelArrow tags and scripts. These are executed on server to generate complete response page before sending these to user's browser. ARO files contain almost 95% of HTML content while the remaining consists of SteelArrow code. For ARO files to work for you, SteelArrow Web Applications server should be installed and running on the web server machine.

## ARO File Format

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web webpages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### ARO Tag Example

The <SAOUTPUT> ARO tag lets developers to output data values at any place within a script. For example, it can be used to get the output of the PARAM table with <SAOUTPUT VALUE=PARAM[]> that can be displayed within the HTML <BODY> tag.

## References

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)
