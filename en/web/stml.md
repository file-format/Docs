{
  "date": "2021-05-20",
  "keywords": [
    "stml",
    "stml file",
    "stml file format",
    "stml file type",
    "file",
    "type",
    "what is an stml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "STML - SSI HTML File",
  "description": "Learn about STML file format and APIs that can create and open STML files.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stml"
    }
  },
  "lastmod": "2021-05-20"
}

## What is an STML file?

A file with .stml extension is a webpage with server side instructions that are executed when a user loads the page in web browser. STML pages contains server side code that contains server side includes to perform tasks that are not possible to achieve with plain HTML. Though similar to [HTML](/web/html/), STML offers more power by running the commands on server, also called Server Side Includes (SSI). With the introduction of new programming languages with server side scripting such as PHP, the use of STML is reduced though it is still supported by all server side technologies. STML files can be opened in any text editor and edited for updating the commands.

## STML File Format

STML is based on plain ascii text file format that is human readable. However,it follows the syntax as defined and exercised using the [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) that are executed on server side. Like any other server side scripting language, STML can use the server side commands to perform tasks such as page visitor counter, web page calendar, retrieve records from database, and similar others.

## STML Example

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
