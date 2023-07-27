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

# HS - Java HelpSet File Format

## What is a Java HS file?

A file with .hs extension in Java programming language is a help documentation file that is used by the JavaHelp system when it is activated by an application. It defines the helpset for the particular application installed and comprises of multiple subsets as part of the system help for the application. The Java program must be able to find the helpset file whose name ends with the .hs extension.

## Java Helpset Information

A .hs file may contain the following information.

|Information|Description|
---|---|
|Map File|The map file is employed to associate topic IDs with the uniform resource locator or path name of hypertext mark-up language topic files.|
|View Information|Information that describes the navigators being employed within the helpset. the quality navigators are: table of contents, index, and full-text search. further navigators include the gloss and also the favourites navigators. data regarding custom navigators is enclosed here further.|
|Helpset title|The \<title> is outlined within the helpset (.hs) file. This title seems at the highest of the most window and any secondary windows outlined in your helpset file.|
|Home ID|The title of the (default) ID that's displayed when the assistance watcher is called without indicating an ID.|
|Presentation|The windows in which to show the assistance subjects. This can be a modern include of the JavaHelp 2 computer program that's portrayed in more detail underneath beneath \<presentation>.|
|Sub-helpsets|This discretionary area statically incorporates other helpsets by utilizing the tag. The helpsets shown by this tag are combined naturally into the helpset that contains the tag. More points of interest around blending can be found in Blending Helpsets.|
|Implementation|This discretionary segment makes a registry that gives key information mapping to characterize the HelpBroker class to utilize within the HelpSet.createHelpBroker method. The registry moreover decides the substance viewer to client for a given Emulate sort.|

## Java HS File Format

The Java HS files are in XML file format and are based on the World Wide Web Consortium (W3C) Extended Markiup Language proposed recommendation [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). This means that a Java HS file is in human readable XML file format that can be opened in any XML reader application.

### Java HS File Format Example

The following is an example of a helpset file as from [Oracle Helpset documentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## References
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script File Format

## What is an HS file?

A file with .hs extension is a Haskell Script file that is written in [Haskell](https://wiki.haskell.org/Haskell), an advanced purely-functional open-source programming language. Code written in HS file is purely based on functions, unlike [C](/programming/c/), [C++](/programming/cpp/) and alike, that follow the principals of rapid development of robust and concise software. Haskell provides built-in concurrency and parallelism along with rich APIs, profilers and debuggers to produce flexible and high-quality applications.

## HS File Format

Like any programming language, HS files are written in plain text format that are human readable. These can be created, edited and viewed with any available text tools. The .hs source code file is compiled with a Haskell compiler, generating the executable binary file.

### HS File Format Example

Code can be written in a .hs file and compiled using a Haskell compiler such as [GHC](https://haskell.org/ghc). The following line of code is saved as `HelloWorld.hs` as shown in the following sample.

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
