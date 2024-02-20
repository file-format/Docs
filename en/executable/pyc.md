{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about PYC file format and APIs that can create and open PYC files.",
  "title": "PYC File Format- Python Compiled File",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-pyc"
    }
  },
  "lastmod": "2022-05-09"
}

## What is a PYC file?

A PYC file is a compiled output file generated from source code written in Python programming language. When PY file is run using Python interpreter, it is converted to bytecode for execution. At the same time, the compiled bytecode is also saved as .pyc file so as to reuse from cache at a later time if applicable.

## Structure of PYC File Format

PYC files are in bytecode and their file format specifications are not available publicly. However, investigation by some sources show that the [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) consists of:

 * `A four-byte magic number` - Simply two bytes that change with each change to the marshalling code, and then two bytes of 0d0a.
 * `A four-byte modification timestamp` - Unix modification timestamp of the source file that generated the .pyc, so that it can be recompiled if the source changes.
 * `A marshalled code object` - the output of marshal.dump of the code object that is a result of compiling the source file.

## FAQs

1. **How is a PYC file generated?** A PYC file is created when Python source code is compiled using the Python interpreter. The compiled code is then stored in the PYC file.

1. **Is PYC faster than py?** PYC files are saved after python source code is compiled. Since these are already interpreted, these files are faster than .py files.

1. **What is the difference between py and pyc file?** PY files contain Python source code file for a program, while .pyc files contain interpreted bytecode of an application.

1. **Is PYC a binary file?** Yes, PYC file is a binary file that contains a 4-byte magic number, a 4-byte modification timestamp, and a marshalled code object.

1. **Can we convert .pyc to .py?** Yes, it is possible to convert pyc files to py. Decompilers such as Decompyle++ may be used to translate compiled Python byte-code back into valid and human-readable Python source code.

## References

* [The structure of .pyc files](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)
