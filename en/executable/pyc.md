{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about PYC file format and APIs that can create and open PYC files.",
  "title" : "PYC File Format- Python Compiled File",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2022-05-09"
}

## What is a PYC file?

A PYC file is a compiled output file generated from source code written in Python programming language. When PY file is run using Python interpreter, it is converted to bytecode for execution. At the same time, the compiled bytecode is also saved as .pyc file so as to reuse from cache at a later time if applicable.

## Structure of PYC File Format

PYC files are in bytecode and their file format specifications are not available publicly. However, investigation by some sources show that the [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.) consists of:

 * `A four-byte magic numbe`r - Simply two bytes that change with each change to the marshalling code, and then two bytes of 0d0a.
 * `A four-byte modification timestamp` - Unix modification timestamp of the source file that generated the .pyc, so that it can be recompiled if the source changes.
 * `A marshalled code object` - the output of marshal.dump of the code object that is a result of compiling the source file.

## References

* [The structure of .pyc files](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)
