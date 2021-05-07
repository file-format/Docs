{
  "date" : "2019-10-11",
  "keywords" : [ "class", ".class","what is a class file","how to open a class file", "extension", "file", "class file","class file format", ".class extension", "class file in java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Class - Java Class File Format",
  "description":"Learn about Class file format and APIs that can create and open Class files.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

## What is a Class file?

A **Class file in Java** is the compiled output of [.java](/programming/java/) class that is actually executed by a Java Virtual Machine (JVM). Class files can be executed individually as well as can be a part of a [JAR](/programming/jar/) file as a bundle along with other package files. These can be created using the **`javac`** command from the command line interface. Some Java IDEs like [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) and NetBeans provide create .class output files from the project's Java files.

## Class File Format

A Java class file comprises of bytecode that is intermediate code to be run by JVM. A class file consists of a stream of 8-bit bytes and multibyte data items are always stored in big-endian order.

### ClassFile Structure

The class file structure is as shown below.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
where:

* u1 = unsigned one-byte quantity
* u2 = unsigned two-byte quantity
* u4 = unsigned four-byte quantity

Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` - The magic item supplies the magic number identifying the class file format; it has the value 0xCAFEBABE.
* `minor_version`, `major_version` - The values of the minor_version and major_version items are the minor and major version numbers of this class file.
* `constant_pool_count` - The value of the constant_pool_count item is equal to the number of entries in the constant_pool table plus one. A constant_pool index is considered valid if it is greater than zero and less than constant_pool_count, with the exception for constants of type long and double.
* `constant_pool[]` - The constant_pool is a table of structures (§4.4) representing various string constants, class and interface names, field names, and other constants that are referred to within the ClassFile structure and its substructures. The format of each constant_pool table entry is indicated by its first "tag" byte.
* `access_flags` - The value of the access_flags item is a mask of flags used to denote access permissions to and properties of this class or interface.
* `this_class` - The value of the this_class item must be a valid index into the constant_pool table.
* `super_class` - For a class, the value of the super_class item either must be zero or must be a valid index into the constant_pool table.
* `interfaces_count` - The value of the interfaces_count item gives the number of direct super interfaces of this class or interface type.
* `interfaces[]` - Each value in the interfaces array must be a valid index into the constant_pool table.
* `fields_count` - The value of the fields_count item gives the number of field_info structures in the fields table.
* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` - The value of the methods_count item gives the number of method_info structures in the methods table.
* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` - The value of the attributes_count item gives the number of attributes (§4.7) in the attributes table of this class.
* `attributes[]` - Each value of the attributes table must be an attribute_info structure.

## How to open a Class file?

Since a Class file is a binary format, it can be open by using any text editor such as Notepad in Windows. However, to get the Java code from a class file, you can either use a decompiler like Java Decompiler or an IDE like Intelli-j with built-in decompiler.

### Softwares that can open the JAR files ###
The JAR files can be opened in the following softwares:

|Software| Operating System|
---|---|
|Oracle Java Runtime Environment|Microsoft Windows, MacOS, Linux|
|Eclipse IDE for Java Developers|Microsoft Windows, MacOS, Linux|
|JD-GUI|Microsoft Windows, MacOS, Linux|
|Jetbrains IntelliJ IDEA|Microsoft Windows, MacOS, Linux|
|dirtyJOE|Microsoft Windows|
|DJ Java Decompiler|Microsoft Windows|


## References

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)
