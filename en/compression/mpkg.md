{
  "date": "2019-10-11",
  "keywords": [
    "mpkg file",
    "mpkg file format",
    "what is a mpkg file",
    "file",
    "mpkg example",
    "mpkg file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MPKG File Format - Meta Package File",
  "description": "Learn about MPKG file format and APIs that can create and open MPKG files.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpkg"
    }
  },
  "lastmod": "2021-04-02"
}

## What is a MPKG file?

A file with .mpkg extension is an archive installer file, mostly found on MacOS Operating Systems. It contains all required installation files of the application without the need to keep associated files separately. A single MPKG file can contain package files [PKG](/compression/pkg/) as one of the installation files in addition to other files. MPKG files can not be opened with any general software and are executed automatically on MacOS using Apple Installer.

## MPKG File Format

An MPKG file contains different types of files that are required for the installation of multiple packages it contains. This is can be seen from the image below which is the tree structure of a sample MPKG file. This tree structure is exported using `tree` command on MacOS terminal.

{{< figure src="../mpkg.png" alt="MPKG File Format" >}}

The description of different elements in the image is as follow.

`Packages Directory` - stores a list of pkg files, that is, a list of sub-Packages
`Resources Directory` - stores resources used by pkg, such as localized resources and images , Rtf documents, pdf documents, etc.
`Distribution.dist file` - An xml document containing information such as sub-packages to be installed and runtime scripts

Sample XML file for an MPKG file can look as follow depending upon the associated sub-packages.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - is the sub-package to be installed. It is a directory of the Bundle structure in pkg format. It contains a Contents subdirectory.

## References

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)
