{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "APPCACHE File - HTML5 Cache Manifest File Format",
  "description": "Learn about what is an APPCACHE file and APIs that can create and open APPCACHE files.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcache"
    }
  },
  "lastmod": "2022-08-05"
}

## What is an APPCACHE file?

An APPCACHE file is a text file that contains the list of resources to be cached by browsers for offline access to the web applications. This is useful when there is no internet connection. In such situation, the browser uses the offline cache resources to provide access to the web contents. APPCACHE file contains web resources such as images (for example **[PNG](/image/png/)**, **[WEBP](/image/webp/)**, etc.), stylesheets **([CSS])(/web/css/)**, and script files (such as Javascript **[JS](/web/js/)** files).

Applications that can **open APPCACHE files** include web browsers such as Google Chrome, Safari, and Firefox.

## APPCACHE File Format - More Information

APPCACHE files are simple text files, providing offline access to web pages for running without an internet connection. The presence of APPCACHE designates a page as available offline.

### How to Reference an APPCACHE file?

In your HTML page, an APPCACHE file is referenced as follow.

```
<html manifest="example.appcache">
  ...
</html>
```

## Structure of an APPCACHE Manifest file

A simple APPCACHE manifest file looks as follow.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

This is a simplest example and there can be more complex structures present as well.

## Advantages of APPCACHE Manifest

The use of cache interface gives web applications the following advantages.

 1. Offline Browsing - The cache interface gives the end users to browse your full site when they're Offline
 1. Speed - cache enables high speed access to offline content directly from disc
 1. Accessibility all the time - In case your site goes down, users will still have access to the web contents and will be able to get the offline experience

## References

 * [A Beginner Guide to AppCache Manifest](https://web.dev/appcache-beginner/)
