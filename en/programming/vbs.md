{
  "date": "2021-08-24",
  "keywords": [
    "vbs",
    "file",
    "extension",
    "file format",
    "Visual Basic Script",
    "Programming Guide",
    "vbs example",
    "Microsoft Visual Basic",
    "VBScript"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "VBS - Visual Basic Script File",
  "description": "Learn about VBS file format and APIs that can create and open VBS files.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbs"
    }
  },
  "lastmod": "2021-08-24"
}

## What is a VBS file?

VBS or VBScript is connected with the script edition of Microsoft Visual Basic. In the computing environment, the user is allowed to access and control many aspects of it. VBScript is allowed to use a model named **Component Object Model** to avail the elements and tools of the environment. This environment is specified for working and running VBScript.

It serves as similar to Javascript when it is accessed by the client in the field of Web development. It is also used by the servers for the processing of web pages. It can be considered in some other types of scripting files such as applications of [HTML](/web/html/). 


## Brief History ##

It was first launched in 1996, as a part of the technologies used by Microsoft specified for Windows Scripts. It was specifically developed for the help of Web developers initially. In the same year, the explorer of Microsoft Windows named Internet Explorer was released along with the features of Visual Basic Script.

With the progress in technology and web development, many versions of VBScript along with many advanced features were launched. Moreover, in the coming year, this scripting language will be part of Microsoft Windows with new features.

## Technichal Specification ##

For the web pages at the server-side, the tools such as **Active Server Pages** are used along with VBScript. This scripting language can also be used in the script component of Windows. The files of this language are stored with a .vbs extension in Windows. 

There are many control structures such as loops that are used in the code of this language. It also includes arguments that are command line and could be named or unnamed. The files of this language can be stored simply in the folders or on the desktop of a Windows operating system. Although there is no specific integrated development environment for VBScript programs like Microsoft Script Editor provide the facility of development of this language.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. The features that involve easy or direct access involves Network Printers, unnamed and named command-line arguments, stdout, and stdin, Network Shares, Windows Management Instrumentation, user information of networks like group membership, and much more. 

## VBS File Format Example ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Reference ##

* [VBS - by Wikipedia](https://en.wikipedia.org/wiki/VBScript)


