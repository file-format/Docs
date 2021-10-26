{
  "date" : "2021-06-28",
  "keywords" : [ "cgi file", "what is a cgi file", "file", "cgi example", "cgi file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about CGI file format and APIs that can create and open CGI files.",
  "title" : "CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2021-06-28"
}

## What is a CGI file?
A CGI file is known as a Common Gateway Interface script that is used by a web server to run an external program to process user requests. The script which saved in a file with .cgi extension is typically written in C or Perl programming languages. The had been introduced since the early days of the Web, when Web developers wanted to connect databases to their Web servers. A server which supported a common gateway between Web server and databases was well suited to execute the CGI code.

## CGI File Format
The CGI scripts are used by the Web server to facilitate the owner to configure how a URL will be handled. The procedure is usually done by marking a new directory (where the documents are mainly located) as containing CGI scripts; its commonly known name is cgi-bin. For example, /usr/local/apache/htdocs/cgi-bin could be picked as a CGI directory on the Web server. When a Web browser requests a URL that points to a file within the CGI directory, then, instead of simply sending that file (/usr/local/apache/htdocs/cgi-bin/printenv.pl) to the Web browser, the HTTP server executes the specified script and return the output of the script to the Web browser. In short, anything that the CGI script is sent to standard output is transferred to the Web client instead of being shown in a terminal of window.

### CGI Example

Following CGI script written in Perl which shows all the environment variables passed by the Web server:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

The output will be like the following:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Uses of CGI scripts
The CGI files containing the CGI scripts are usually used to process input data from the user and produce the relevant output data. Implementing a wiki is one of the examples of CGI program. If the user agent sends a request for the name of an entry, the Web server runs the CGI program. The CGI program get the source of that entry's page, convert it into HTML, and prints the result. The Web server receives the output from the CGI program and return it to the user agent. Then, if the user agent calls the edit function by clicking "Edit Page" button, the CGI program shows an HTML textarea or other editing control with the page's contents. Finally, if the user agent clicks the "Publish page" button, the CGI program converts the updated HTML into the source of that entry's page and saves it.



## References 

* [Common Gateway Interface - by Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)
