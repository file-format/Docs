{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HTACCESS File - Apache HTACCESS File Format",
  "description" : "Your file format guide to learn what is an HTACCESS file",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an HTACCESS file?

An HTACCESS file is an Apache configuration file that provides a mechanism to allow configuration changes for different folders/directories of a website. It includes configuration directives that are applicable to the directory and sub-directories.

An HTACCESS file performs a number of checks such as defining the index page of a website, listing the 404 (Page Not Found) error page, performing the 301 or 302 page redirects, blocking access from a specific IP address or other websites. The use of .htaccess files, thus, slows down the overall performance of your Apache [HTTP](/web/http/) server.

## HTACCESS File Format

HTACCESS files are stored to disc in plain text file format. This means you can open and edit these files in any text editor. There is no name before the "." in an .htaccess file, showing that it is a hidden file within the folder.

## Common uses of an HTACCESS File

Five common uses of an HTACCESS file are as follow.

### Mod_Rewrite

An HTACCESS file can be used to designate and alter how URLs and web pages on a website are displayed to the users.

### Authentication

Authentication can be achieved with .htaccess by creating a passowrd file called .htpasswd. This lets the site visitors to provide a password if they would like to visit a certain section of the webpage.

### Custom Error Pages

You can create custom error pages such as 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found and 500 Internal Error with .htaccess file. However, these will slow down the sever performance as these all checks will be executed as the pages are accessed.

### MIME Types

Apache HTACCESS files can be modified to include Multipurpose Internet Mail Extensions (MIME) types. This lets your server to support delivery of application files that were not supported by the site.

### SSI

Server Side Includes (SSI) act as a great time-saver on a website. SSI can be enabled by inserting hte following code into your .htaccess file.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS File Example

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## References

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)
