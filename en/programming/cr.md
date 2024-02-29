{
  "date" : "2024-03-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CR File - Crystal Source Code - What is .cr file and how to open it?",
  "description" : "Learn about CR Crystal Source Code File and how to open it.",
  "linktitle" : "CR",
  "menu" : {
    "docs" : {
      "identifier" : "programming-cr",
      "parent" : "programming"
    }
  },
  "lastmod" : "2024-03-08"
}

## What is a CR file?

A CR file typically refers to a Crystal programming language source code file. Crystal is a statically-typed, compiled language with syntax inspired by Ruby. Here is a simple example of what a CR file might contain:

```
# This is a comment
class Greeter
  def initialize(@name : String)
  end

  def greet
    puts "Hello, #{@name}!"
  end
end

greeter = Greeter.new("World")
greeter.greet
```

Crystal is a statically-typed, compiled programming language with Ruby-like syntax, offering high performance and type safety. It supports concurrency, metaprogramming, and emphasizes safety. Crystal is cross-platform and has a growing ecosystem of libraries and frameworks.

## How to open a CR file?

To open a CR file, you can use any text editor or integrated development environment (IDE) that supports Crystal syntax highlighting and editing. Here are some common options:

1.  **Visual Studio Code**: Install Crystal Language extension for syntax highlighting and other language features.
    
2.  **Atom**: Install language-crystal package for Crystal language support.
    
3.  **Sublime Text**: Use Crystal Language package for syntax highlighting and other Crystal-specific features.
    
4.  **Vim**: Install a plugin like vim-crystal for Crystal syntax highlighting and editing support.
    
5.  **Emacs**: Install a package like crystal-mode for Crystal syntax highlighting and editing capabilities.
    

Once you have one of these editors or IDEs set up, you can simply open the `.cr` file as you would any other text file, and you'll be able to view and edit the Crystal source code.

## References
* [Crystal (programming language)](https://en.wikipedia.org/wiki/Crystal_(programming_language))
