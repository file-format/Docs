{
  "date": "2021-05-20",
  "keywords": [
    "shtml",
    "shtml file",
    "shtml file format",
    "shtml file type",
    "file",
    "type",
    "what is an shtml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "SHTML - Server Side Include HTML File",
  "description": "Learn about SHTML file format and APIs that can create and open SHTML files.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtml"
    }
  },
  "lastmod": "2021-05-20"
}

## What is an SHTML file?

A file with .shtml extension is a webpage that is written in [HTML](/web/html/) and includes server instructions. It may also contain server-side includes similar to ASP files for faster loading. The server side files can also contain executable code that can make the server to load slower than usual. SHTML files are similar to HTML but they also allow the use of simple server commands. These server commands are performed in a simple computer programming language called Server Side Includes (SSI). SHTML has been largely superseded by other server side programming languages such as [PHP](/programming/php/) includes.

## SHTML File Format

SHTML files are written in plain text and use the [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) that are executed on server side. These server side commands can be used to even connect to database using the database drivers and fetch users data from tables.

## SHTML Example

Server side instructions are used in applications such as for page visitor counter or web page calendar. The following example, displays the first four columns of the first three lines of the users database.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## References

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)
