{
  "date" : "2019-10-11",
  "keywords" : [ "asax","asax file", "asax file format", "asax file type", "file", "type", "what is an asax file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ASAX - ASP.NET Server Application File",
  "description" : "Learn to know what is an ASAX file and APIs that can create and open ASAX files.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-06-07"
}

## What is an ASAX file?

A file with .asax extension is a file used by ASP.NET applications that resides on the server side. It contains code for responding to application-level and session-level events raised by ASP.NET or by HTTP modules. This also includes handling certain events when the application launches or shuts down. ASAX files are optional and only a single ASAX file is added to web applications to handle the application-level events and errors at the global level. Unlike ASPX pages, ASAX files do not contain any code to implement the functionality of the application.

## ASAX File Format

ASAX files are written in plain text file format and are human readable. The most commonly used ASAX file is Global.asax that resides in the root directory of an ASP.NET application. Web Servers are configured to reject any incoming calls to this file to forbid users from downloading or viewing the code of this file.

### Global.ASAX - An Example of ASAX File Format

A single ASAX file consists of multiple sections that are written to handle the application-level events. These are as follow.

 * **Application Directives** - Application directives are tags that are used to define optional application-specific settings to be used by the ASP.NET parser when processing the Global.asax file. These directives are located in the start of the Global.asax file and are defined as follow.

 ```
 <%@ directive attribute=value [attribute=value … ]%>
 ```
 * **Code Declaration Blocks** - Code-declaration blocks are used to define sections of server code that are embedded in ASP.NET application files within the \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
      }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
 * **Code Render Blocks** - These define the inline code or expressions that execute when the page is rendered. The two styles of code render blocks include inline code and inline expressions. The former is used to define self-contained lines or blocks of code, while the lateral is used as a shortcut for calling the Write method.

## References

 * [HTTP Handlers and HTTP Modules Overview](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Syntax](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))
