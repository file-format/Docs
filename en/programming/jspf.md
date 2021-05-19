{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JSPF - JSP Fragment File Format",
  "description":"Learn about JSPF file format and APIs that can create and open JSPF files.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-21"
}

## What is a JSPF file?
The file with .jspf extension is called JSP fragment; a static file included in another JSP file. The JSPF files are not compiled on their own, however, they are compiled along side the page in which they included. Its syntax is similar to the Java Server Pages (JSP) code. It contains just a fragment of JSP; not included all the entire JSP document. 

## JSPF file format
The term "JSP segment" is used instead as the term "JSP fragment" is overloaded in the JSP 2.0 Specification. The JSP fragments can use either .jsp or .jspf extensions and should be placed either in **/WEB-INF/jspf** or with the rest of the static files. The JSP fragments that are not complete pages must use the .jspf extension and must be placed in **/WEB-INF/jspf** 

## JSP or JSP Fragment File Organization
A JSP file contains the following sections in the order they are listed:

1. Opening comments
2. JSP page directive(s)
3. Optional tag library directive(s)
4. Optional JSP declaration(s)
5. HTML and JSP code

A JSP or JSPF file both begins with a server side style comment which is called **Opening Comment**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
This comment can be visible only on the server side because it is removed during JSP page rendering.

## When to use JSP Fragment file?
When a JSP page requires a certain but complex structure which may also re-use in other JSP pages, one way to handle this is to break it up into pieces, using the Composite View pattern (the Patterns section of Java Blueprints). For example, a JSP page sometimes has the following logical layout in its presentation structure:

{{< figure src="../jspf.png" alt="JSPF File Format" >}}

In this situation, this composite JSP page can be converted into various modules, each will be called a separate JSP fragment. The JSP fragments can then be placed in appropriate locations in the composite JSP page. Hence, the JSPF file are used when static include directives are used to include a page that would not be called by itself, the files with .jspf extension should be placed in the /WEB-INF/jspf/ directory of the Web application archive (war). 

## JSPF Example
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## References

 * [Code Conventions for the JavaServer Pages](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
