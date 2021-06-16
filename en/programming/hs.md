{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HS - Haskell Script File Format",
  "description":"Learn about what is a HS file format and APIs that can create and open HS files.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-06-15"
}

## What is an HS file?

A file with .hs extension is a Haskell Script file that is written in [Haskell](https://wiki.haskell.org/Haskell), an advanced purely-functional open-source programming language. Code written in HS file is purely based on functions, unlike [C](/programming/c/), [C++](/programming/cpp/) and alike, that follow the principals of rapid development of robust and concise software. Haskell provides built-in concurrency and parallelism along with rich APIs, profilers and debuggers to produce flexible and high-quality applications.

## HS File Format

Like any programming language, HS files are written in plain text format that are human readable. These can be created, edited and viewed with any available text tools. The .hs source code file is compiled with a Haskell compiler, generating the executable binary file.

### HS File Format Example

Code can be written in a .hs file and compiled using a Haskell compiler such as [GHC](http://haskell.org/ghc]. The following line of code is saved as `HelloWorld.hs` as shown in the following sample.

```
main = putStrLn "Hello, World!"
```

This is compiled using the command:

```
$ ghc -o hello hello.hs
```
and resulting execuable file can be run as:

```
$ ./hello
```
This prints the "Hello, World!" statement to the output.

## References

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell In 5 Easy Steps](https://wiki.haskell.org/Haskell_in_5_steps)
