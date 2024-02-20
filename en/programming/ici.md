{
  "date": "2021-09-13",
  "keywords": [
    "ici",
    "file",
    "extension",
    "file format",
    "ICI implementation",
    "Programming Guide",
    "ici example",
    "ICI programming language",
    "modules of ICI",
    "data model of ICI",
    "documentation of ICI",
    "ICI language"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "ICI - Programming Language File",
  "description": "Learn about ICI file format and APIs that can create and open ICI files.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ici"
    }
  },
  "lastmod": "2021-09-13"
}

## What is an ICI file?

A general-purpose programming language that is interpreted and contains several features such as dynamic typing along with the flexible data types is known as ICI (not an acronym) programming language. It is considered to be similar to the [Perl](/programming/pl/) language. This ICI language comprises flow control constructs and also contains some operators of the C language. It is not an object-oriented language but some of the features of OOP can be attained by a specific inheritance method known as superstructures. Similar to [C](/programming/c), this ICI programming language has the same system interface and a standard library for built-in functions.


## Brief History ##

In the late 1980s, it was developed by Tim Long as a general-purpose interpreted programming language. Most of the features of this language are similar to C and it can also achieve some of the features by applying some special methods. This language is owned as a public domain and is available as a resalable language and no one is bound to mention where he got the source code from. The documentation of ICI is under the copyright of Canon Information System Research Australia.

## Technichal Specification ##

There are two different data types used in this language. These two are Primitive and Aggregate data types. Both of these include different expressions according to their pre-defined composition in the language. Different modules such as nested and subroutines are supported by this language. As some of its properties are similar to Perl it has a strict integration with the regular expressions.

Sets are confined to be heterogeneous and nested. These sets provide support for commonly used set operations such as Union and Intersection etc. It is mostly used as a language for the sake of core implementation for applications owned by multinational organizations. 

Almost all types of programs can be written in this language and mostly the specific programs which involve complex data structures are written in the ICI programming language. Applications can involve the ICI implementation in a way that they should be written in it. Functional portions of the application can be implemented by the modules of ICI. The language of ICI resembles somewhat C language but the data model of ICI is quite higher level and different with types like dictionaries (struct), sets, dynamic arrays, regular expressions, and (real) strings.


## ICI File Format Example ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Reference ##

* [ICI Programming Language](http://atrn.org/ici/doc/ici.html)


