
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "4th File - Forth Language File Format",
  "description":"Learn about what is .4th file format with example and APIs that can create and open 4th files.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-02-09"
}

## What is a 4th file?

A file with .4th file extension is a programming file created for the **Forth Programming Language**. It contains source code for programs written in Forth programming language and generates the output when the program is executed. It is just another programming language file similar to [C](/programming/c/) and [C++](/programming/cpp/) source file.

## 4th File Format - More Information


### 4th Programming Language Code Example

Here is an example of a simple program written in Forth that calculates the factorial of a given number:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * multiplies the two values on top of the stack. The if and begin/until constructs control the flow of the program.

To use this program, you would enter the definition into the Forth interpreter, and then call the factorial word with the number you want to find the factorial of:

```
10 factorial .
```
This would result in the output 3628800, which is the factorial of 10.

## References

 * [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))
