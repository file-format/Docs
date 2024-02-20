{
  "date": "2021-12-09",
  "keywords": [
    "asa",
    ".asa",
    "file format",
    "file type",
    "what is a .asa file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASA - ASP Configuration File",
  "description": "Learn about what is an ASA file and APIs that can create and open ASA files.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa"
    }
  },
  "lastmod": "2021-12-09"
}

## What is an ASA file?

An ASA file is configuration file, created for [ASP](/web/asp/)/ASP.NET projects. It contains declarations of variables, contains and functions that are meant to be accessible on Global level in the application. All the pages in the project can access these variables and functions, thus avoiding the requirement of rewriting these. One such example is the Global.asa page that is stored in the root directory to be accessible by other ASP website pages. Global.asa files are optional, but if used, each application can have only one Global.asa file.

## ASA File Format - More Information

ASA files are plain text files with the following information.

 * Application events
 * Session events
 * \<object> declarations
 * TypeLibrary declarations
 * the #include directive

## ASA File Example

A Global.asa file could look something like this.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## References

* [ASP Global.asa file - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)
