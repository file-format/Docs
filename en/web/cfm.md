{
  "date": "2021-07-13",
  "keywords": [
    "CFM",
    "extension",
    "file",
    "format",
    "system",
    "Cold Fusion Markup Language",
    "language",
    "CFM web pages",
    "CFML engine",
    "CFML"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "CFM - Cold Fusion Markup",
  "description": "Learn about CFM file format and APIs that can create and open CFM files.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm"
    }
  },
  "lastmod": "2021-07-13"
}

## What is a CFM file? ##

The web pages and files used in **Cold Fusion Markup Language** contain extensions of CFM and are named CFM web pages. This web development scripting language runs on Google App Engine, .NET framework, and JVM. It can contain a programming language or code of the language. When any of its pages are accessed by the user, the webserver of ColdFusion executes it. CFScript (that is close to JavaScript) or tags can be used to write CFML. CFML can be used for generating other languages apart from [HTML](/web/html/) like [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/), and more.

The use of this language and tags that it supports is mostly in developing dynamic web applications The files can be directly run in the browser online if any error occurs during offline usage of the platform of development of the application.
 
CFML works in a way that specific server file extensions (.cfc, .cfm) are given for processing to the CFML engine. If the engines are based on Java, it is achieved using Java servlets. The engine of CFML only processes functions and tags and it returns functions and text outside the CFML tags to the webserver without any change.


## Brief History ##

In 1995, it was first created by a corporation named Allaire. In 2005 Adobe acquired it and it provides services for developing ColdFusion still now. By the passing years, it got developed and upgraded by many people and companies. In 2012, a foundation named OpenCFML was launched. Later on,  in 2015 the former Railo provided his services to improve the performance of CFM and made the resources fewer for better functionality. The most recent update of it was launched in 2020 which is announced to be continued until 2028.

## CFM File Format ##

The code of the CFM files and web pages mostly comprises the tags like HTML but with a slight difference. These files are responsible for performing various operations that ColdFusion scripts enable to run.
*	These files can be accessed and run directly on both Windows and macOS using the browser of any operating system.
*	Adobe ColdFusion provides the platform for the development of web pages and dynamic applications on PC.
*	Any text editor like NotePad or any other text editor in an operating system can be used to open these files as these files are text-based.
*	When any CFM file is opened in a text editor it displays code that consists of the tags and scripts that one would not understand unless he is a web developer.

## CFM Usage Example ##

The following shows a simple usage example CFM file.

### CFM Document ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## References ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)
