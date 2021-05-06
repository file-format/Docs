{
  "date" : "2019-10-11",
  "keywords" : [ "JAR", ".jar","what is a jar file","how to open a jar file", "extension", "file", "jar file","jar file format",  ".jar extension" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JAR - Java Archive File Format",
  "description":"Learn about JAR file format and APIs that can create and open JAR file.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

## What is a JAR file?

A file with .jar extension is a Java Archive file that contains many different application related files as a single file. This file format was created to reduce the speed of loading a downloaded Java Applet in browser via HTTP transaction, by avoiding to create multiple HTTP connections. A single JAR file can contain Java class files ([.class](/programming/class/)), [images](/image/), and [sounds](/audio/). Individual items inside a JAR file can be digitally signed by the application developer to authenticate their origin. JAR files are regularly used to create functional APIs that contain specific functionality related to that API.

## JAR File Format

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### The Manifest File

When a JAR file is created, a manifest file is automatically created inside it that contains the metadata information about the contents of the JAR file. This file shows the contents that are packaged inside the JAR file. A typical Manifest file looks as follow which shows the folders and classes included in the JAR file.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest Specifications

Manifest specifications are defined by Oracle as follow.

`manifest-file`: main-section newline \*individual-section

`main-section`:  version-info newline \*main-attribute

`version-info`:  Manifest-Version : version-number

`version-number` : digit+{.digit+}*

`main-attribute`:  (any legitimate main attribute) newline

`individual-section`: Name : value newline \*perentry-attribute

`perentry-attribute`: (any legitimate perentry attribute) newline

`newline` : CR LF | LF | CR (not followed by LF)

`digit`: {0-9}

### Executable JAR

JAR files can also comprise of an application that can be executed by Java Virtual Machine (JVM) similar to any other application on Microsoft Windows Operating System. In this case, the JVM needs to know about the application's entry point that is any class with a public static void main method. The manifest file identifies such a class with `Main-Class` header in the following format:

```
Main-Class: com.example.MyClassName
```
## How to open a JAR file?
In order to open a JAR file, the Java Runtime Environment must be installed. Alternatively, the JAR files can be opened with archiving applications such as WinZip, WinRAR and 7-ZIP.
### Softwares that can open the JAR files ###
The JAR files can be opened in the following softwares:

|Software| Operating System|
---|---|
|Oracle Java Runtime Environment|Microsoft Windows, MacOS, Linux|
|Oracle Java SE Development Kit|Microsoft Windows, MacOS, Linux|
|Corel WinZip|Microsoft Windows, MacOS|
|7-Zip|Microsoft Windows|
|RARLAB WinRAR|Microsoft Windows|



## References

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR File Format](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for%20distribution.&text=They%20are%20built%20on%20the,jar%20file%20extension.)
