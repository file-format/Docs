{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WHL File Format - Python Wheel Package File",
  "description": "Learn about WHL file format and APIs that can create and open WHL files.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-whl"
    }
  },
  "lastmod": "2022-06-29"
}

## What is a WHL file?

A WHL (Wheel) file is a distribution package file saved in Python's wheel format. It is a standard format installation of Python distributions and contains all the files and metadata required for installation. The WHL file also contains information about the Python versions and platforms supported by this wheel file. Similar to an [MSI](/executable/msi/) setup file, WHL file format is a ready-to-install format that allows running the installation package without building the source distribution.

## WHL File Format

WHL file format is a [ZIP](/compression/zip/) (.zip) archive that contains all the installation files and metadata required by installers for installation of a package. These WHL files can be extracted using unzip option or standard decompression software applications such as WinZIP and WinRAR.

### WHL File Name Convention

A WHL file is named as per the following convention.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

An example of the WHL file name is as follow.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * `cryptography` is the package name.
 * `2.9.2` is the package version of cryptography. A version is a PEP 440-compliant string such as 2.9.2, 3.4, or 3.9.0.a3.
 * `cp35` is the Python tag and denotes the Python implementation and version that the wheel demands.
 * `abi3` is the ABI tag. ABI stands for application binary interface.
 * `macosx_10_9_x86_64` is the platform tag, which happens to be quite a mouthful.

## References

* [What Are Python Wheels and Why Should You Care?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)
