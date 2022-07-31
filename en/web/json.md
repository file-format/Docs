---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON File Format - What is a JSON file?
linktitle: JSON
description: Learn about JSON file format and APIs that can create and open JSON files.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## What is a JSON file?

JSON (JavaScript Object Notation) is an open standard file format for sharing data that uses human-readable text to store and transmit data. JSON files are stored with the .json extension. JSON requires less formatting and is a good alternative for [XML](/web/xml/). JSON is derived from JavaScript but is a language-independent data format. The generation and parsing of JSON is supported by many modern programming languages. *application/json* is the media type used for JSON.

## JSON File Format - Brief History

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON was based on Standard ECMA-262 3rd Edition—December 1999 which is a subset of JavaScript.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. In November 2017, ISO/IEC 21778:2017 was published as an international standard. RFC 8259 was published on 13 December 2017 by The Internet Engineering Task Force which is the current version of the Internet Standard STD 90.

## JSON File Structure

JSON data is written in **key/value** pairs. The key and value are separated by a colon(:) in the middle with the key on the left and the value on the right. Different key/value pairs are separated by a comma(,). The key is a string surrounded by double quotation marks for example "name". The values can be of the following types.

- `Number`
- `String`: Sequence of Unicode characters surrounded by double quotation marks.
- `Boolean`: True or False.
- `Array`: A list of values surrounded by square brackets, for example

    ```json
    [ "Apple", "Banana", "Orange" ]
    ```

- `Object`: A collection of key/value pairs surrounded by curly braces, for example

    ```json
    {"name": "Jack", "age": 30, "favoriteSport" : "Football"}
    ```

JSON objects can also be nested to represent the structure of the data. Given below is an example of a JSON object.

### JSON Format Example

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## What is the maximum size of JSON file?

There is practically no limit on the maximum size of a JSON file. It can be as long as the space required by the contents to be stored.

When it comes to using JSON file format for transferring data over the internet, one needs to be careful about the available resources of computer. If large JSON data is transferred, the transfer will be affected if the client browser has limited memory.


There is no hard limit defined by specification, but you need to be careful not to exhaust resources on your users’ computers, as it will quickly degrade their user experience, and they will be likely to abandon your app.

## JSON vs XML

**XML** is another common and widely used file format for exchange of data over the internet. When it comes to exchange of data between applications, developers have option of using both XML and JSON file formats. However, JSON is adopted as the most convenient way for data exchange between applications over the internet due to the following reasons.

 1. JSON gives a clear and easier to read view of data as compared to XML file formats
 1. JSON reduces the overhead of data transfer over the internet as it has less number of characters to define the same set of data as compared to XML
 1. Modern programming languages provide builtin parsers to parse the JSON response over the web.

## Did you know?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## References

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)
