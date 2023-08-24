{
  "date" : "2021-07-08",
  "keywords" : ["HAR", "File", "Extension", "File Format", "File Extension", "JSON", "Archive File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HAR - HTTP Archive File Format",
  "description" : "Your file format guide to learn what is a HAR file and APIs that can create and open HAR file.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-07-08"
}

## What is a HAR file?

A file with .har (HTTP Archive) file is an HTTP archive file that stores session data transferring over many browsers (such as Chrome, Safari, IE, Firefox, etc.) in [JSON](/web/json/) file format. The data transferred over the internet between the server and the client (in this case user's browser) contains HTTP request and response headers that are stored in HAR file. It further contains detailed information about performance data about web pages loaded in the browser. HAR files can be opened in any text editor such as Notepad on Microsoft Windows OS and TextEdit on Apple MacOS.

## HAR File Format - More Information

HAR files store session information in plain text file using the popular JSON format. The specifications for HAR file format were produced by the Web Performance Group of the World Web Consortium (W3C) but could not be published. However, it successfully defined an archival format for HTTP transactions.

In addition to monitoring the transfer of request and response information, HAR files are used by developers to log the web browser's performance in terms of page load speed, content load duration, content loaded, queries executed to get the response from browser, and many other.

## Why to use HAR files?

HAR files can be helpful in improving a website's performance by evaluating long load times, page rendering times, and response times. HAR files can be analyzed to find any such issues and solve any issues with the website for improving performance.

## How to generate HAR file?

So, how to generate a HAR file? Well, this depends on what type of browser you are using to generate a HAR file. In this guide, we are listing the steps for Google Chrome browser. Methods for generating HAR files using Safari, Firefox, etc. can easily be searched on the internet and followed.

### Steps to Generate HAR file using Google Chrome

The following steps can be carried out on a web page where issues are being faced.

 1. Open the web page in Google chrome where the problem happened.
 1. Open the developer tool (inspect element).
 1. Go to the left of the panel to start the file recording. There is a small round red button in this section.
 1. Click the to “Clear icon” to delete any log records kept in the browser.
 1. To save the content you want as shown above, right click and click “Save as HAR File”

## References

* [HAR File Format - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))
