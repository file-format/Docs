{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CFML - ColdFusion Markup Language File",
  "description" : "Learn about what is a CFML file and APIs that can create and open CFML files.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-08-19"
}

## What is a CFML file?

A file with .cfml extension is a ColdFusion Markup Language file that is used to create web page. It refers to a set of rules used to define how the ColdFusion application will be developed by the programmer. ColdFusion is a programming language that is used to to create sever-side web applications quickly and with less than other technologies such as [ASP](/web/asp/), [PHP](/web/php/), etc. Some of the applications that can open CML files include Adobe ColdFusion 2018, Adobe ColdFusion Builder, and Adobe Dreamweaver.

## CFML File Format - More Information

CFML files are markup files and contain web elements in the form of tags. These are text files that can be opened and edited in any text editor. CFML files consist of several tags that are similar to [HTML](/web/html/) and usually comprise of an opening and a closing tag. These tags can also contain one or more attributes.

### Tags Syntax

Following is the generalized syntax of CFML tags.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Most tags accept attributes and are defined as follow.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Some of these tags also accept multiple attributes with the following syntax.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML Code Example

Here's an example that uses an actual CFML tag - the `cfoutput` tag:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## References

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)
