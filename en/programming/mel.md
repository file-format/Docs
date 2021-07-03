{
  "date" : "2019-10-11",
  "keywords" : [ ".mel", "Maya Embedded language","file", "extension", "file format", "Maya 3D", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MEL - Maya Embedded Language File Format",
  "description":"Learn about MEL file format and APIs that can create and open MEL files.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-03-08"
}

## What is a MEL file?

A file with .mel (Maya Embedded Language) extension is a scripting language that is used by Autodesk Maya to create graphical interfaces. It lets you automate the creation of graphical elements using executable scripts in addition to Maya's graphical interface. MEL empowers you to create graphical interfaces without learning programming. This is achieved by creating Macros and custom actions that speed up repetitive tasks. These procedures and scripts let you create custom modelling, animations, dynamics and tasks rendering. Autodesk Maya 2020 can be used to open and view contents of an EML file.

## MEL File Format - More Information

A programmer's [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) is available for developers on Maya's documentation section. MEL is based on shell scripting commands, similar to UINX, to achieve things. The scripting based commands makes it irrelevant to conventional and object oriented programming (OOP), resulting in no usage of data structures, calling functions, or using OOP as in other languages.

Some key points about MEL are as follow.

`Comments` - Every statement in MEL must end with a semi-colon (;), even at the end of a block.

`Returning Values` - Stating an expression that returns a value does not automatically print the value in MEL. Instead it causes an error.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Commands for Create, Edit and Delete` - The same command is used to create things, edit things or query information about existing things. However, a flag controls what (create, edit, or query) the command does.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - Function syntax automatically returns a value. To get a return value using command syntax, you must enclose the command in backquotes.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## References

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)
