{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VPK File - PlayStation Vita Application Package File Format",
  "description":"Learn about VPK file format and APIs that can create and open VPK files.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-03-01"
}

## What is a VPK file?

A file with .vpk extension is a compressed archive package file that is used to install third-party apps on Sony PlayStation Vita gaming console. These files can be installed only on jailbreak Vita PlayStation by HENkaku that enabled the PS Vita and PSTV to use customized user created content. A VPK archive file contains all the contents that make up the game including images such as [PNG](/image/png/) files, setting files such as [.bin](/disc-and-media/bin/), and any configurations in [XML](/web/xml/) file format.

## VPK File Format

VPK files are saved to disc as standard compressed [ZIP](/compression/zip/) archives. These may contain multiple folders and other associated files for the third-party apps to be installed on Vita Gaming Console. To view the contents of the VPK package file, rename its extension from .vpu to .zip, and extract the contents using standard decompression utilities such as WinZip or WinRAR.

Valvesoftware has detailed information about the [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format) that can be referenced from developer's perspective.

## How to Install VPK files?

The VPK files can be installed from the command line utility VPK.exe. On Windows OS, files can be dropped on vpk.exe file which returns a \*.vpk containing all the packaged files. Alternatively, the command line tool can be used as follow.

### Create VPK and Add Files

```
vpk <dirname>
```

### Extract VPK Files

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## References

* [VPK File Format](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK Files](https://developer.valvesoftware.com/wiki/VPK)
