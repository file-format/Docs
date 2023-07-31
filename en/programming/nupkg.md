{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "NUPKG File - NuGet Package File",
  "description":"Learn about NUPKG file format and APIs that can create and open NUPKG files.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-03-09"
}

## What is a NUPKG file?

A NUPKG file is a package file that contains source code to be used by NuGet software for creating packages to be used in .NET projects. NuGet Package Manager component is installed as part of Microsoft Visual Studio for fetching packages from online packages hosting repository. NUPKG files help developers fetch the latest packages from [Nuget.org](https://nuget.org) using NuGet Package Manager instead of manually downloading and installing the development packages. NUPKG files are built from NUSPEC files and, when fetched, install the package on user system.

## NUPKG File Format

NUPKG files are [ZIP](/compression/zip/) archives that contain the packaged libraries inside it. When downloaded, it can be renamed to .zip and extracted with any standard zip utilities like WinZIP, 7-Zip, and Apple Archive Utility.

## Reference

* [Nuget.org](https://nuget.org)
* [Quickstart: Install and use a package in Visual Studio (Windows only)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [How to Create and Publish a Nuget Package](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)
