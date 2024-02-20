{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HTX File - HTML Extension File Format",
  "description": "Your file format guide to learn what is an HTX file and APIs that can create and open HTX file.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htx"
    }
  },
  "lastmod": "2019-09-10"
}

## What is an HTX file?

An HTX file is actually an HTML file that contains data variables for displaying the database query results as a webpage. Mostly created with Microsoft FrontPage Web development software, HTX files are saved to be saved in the same folder as the corresponding Internet Database Connector (.IDC) file.

HTX files can be opened with applications such as Microsoft FrontPage and any text editor such as Notepad, TextEdit, or Atom.

## HTX File Format

HTX files are saved as plain text file with code for retrieving data from a database and saving in variables for display.


### HTX File Example

An example of HTX file is as follow that defines a page header for displaying the query restriction and the documents displayed on the page for displaying to user.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

The output of this sample code is as follow.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

As can be seen, the HTX file is a template that formats how results are returned and displayed to the end users. It is written in the HTML format with some IIS extensions and Indexing Service. These extensions include variable names and other codes for processing results.

## References

* [Formatting the Results in .Htx File](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)
