{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "M - Matlab Source Code File",
  "description":"Learn about Matlab .m Source Code file and APIs that can create and open MF files.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

## What is an  M (Matlab) file?

A file with .m extension is a source code file used by Matlab, a programming and numeric computation platform used for analysis, algorithms development, and simulation modelling. Like other programming file formats, an M file contains source code that executes Matlab commands to plot graphs, run simulations, and other mathematical operations. A single Matlab simulation can span over multiple such .m files that can classify the application in scripts, classes, functions, or declarations. Matlab M files can be opened with any text editor.

## Matlab M File Format - More Information

Matlab .m files are text files that contain programming code in Matlab programming language. These can be opened and edited in any text editor, and saved back to be executed in Matlab software. Matlab itself contains a Live Editor that is used for creating scripts that is a combination of code, output, and formatted text.

### Matlab Function Files

Like other programming languages, you can create a .m file that only contains the definition of a function which performs a specific task only. Such files are also saved with .m extension and implements the functionality related to that function only.

## .M File Example

The following is a Matlab function file example that calculates the time taken for an object dropped from height h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

To call this function from Matlab editor or from another .m file, the following code can be used.
```C++
TimeToGround(100)
```

## References

 * [Matlab - Supported File Formats](https://www.mathworks.com/help/matlab/import_export/supported-file-formats.html)
 * [Using Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)
