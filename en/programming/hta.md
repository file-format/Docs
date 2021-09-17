{
  "date" : "2021-09-16", 
  "keywords" : [ "hta", "file", "extension", "file format", "hta implementation", "Programming Guide", "hta example", "HTML Application", "Hypertext Markup Language Application", "HTA files", "Microsoft HTML Application"],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HTA - HTML Application Files",
  "description":"Learn about HTA file format and APIs that can create and open HTA files.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-09-16"
}

## What is an HTA file?

The HTMLA stands for **Hypertext Markup Language Application** is a program that is compatible with Microsoft Windows. The source code of this program includes more than one scripting language such as [HTML](/web/html/) and [JavaScript](/web/js/). For the user interface, an HTML Application is preferred while to fulfill the requirement of program logic any other scripting language is used.

An HTML Application is independent of the security model of the internet browser and runs as a fully trusted application. The extension used for files regarding these applications is HTA. These applications include features of HTML along with the properties of other scripting languages.


## Brief History ##

The HTA was first introduced in 1999 by Microsoft along with the release of Internet Explorer 5. It was compatible with Internet Explorer and so could be executed on Windows operating system only. This technology was patented in 2003. The HTA files are executed as similar to any other .exe files. The HTA files are compatible with today's updated version of Windows 11 as well.


## Technichal Specification ##

HTAs have the same format as any other HTML page comprises of, while some attributes are used for controlling the styles of borders or icons of programs. Moreover, arguments are provided for the launch of HTA. These applications can be executed using a program named mshta.exe. It can be accessed by simply double-clicking on the file. These programs automatically run along with the Internet explorer. Besides other specifications, these are not independent of the Trident engine browser but are independent of Internet Explorer. It means that these can be executed without using Internet Explorer.

The tags are used for the sake of customization of the appearance of these applications. The conversion from Microsoft HTML application to HTA format is easier i.e you only need to change the extension. As we know that these applications are fully trusted so these comprise more features and advantages as compared to simple HTML files. Text editors can be used to create HTA. These editors can be acquired by Microsoft or any other trusted source.


## HTA File Format Example ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Reference ##

* [HTA - by Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)


