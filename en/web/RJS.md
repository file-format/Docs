{
  "date" : "2021-05-24",
  "keywords" : ["rjs", "File", "Extension", "File Format", "File Extension", "RJS", "Ruby Javascript File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RJS - Ruby Javascript File",
  "description":"Learn about what is RJS file format and APIs that can create and open RJS files.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-24"
}

## What is an RJS file?

A file with .rjs extension is a combination of Ruby code and JavsScript that allows Rails developers to use Ruby to produce dynamic JavaScript code. Ruby code is embedded in Java functions and is compiled on the web server that requires Ruby engine to be to be running on the server. RJS is similar to [RHTML](/web/rhtml/); the only difference is that the lateral contains Ruby code in [HTML](/web/html/) while it contains Ruby code in Javascript functions.

## RJS File Format

RJS files are coded in plain text like any other scripting or programming language. When such a page is requested by client, the Ruby code is executed on server, and only HTML and Javascript code are returned to client's browser. The syntax of RJS file is similar to that of combination of Ruby and JavaScript syntax such that only the Ruby code is embedded in JavaScript functions.

### RJS Example

The following example shows a simple Ruby code independently and then embedded in a JavaScript function.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
and following is the RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## References

* [RJS](https://github.com/makevoid/rjs)
