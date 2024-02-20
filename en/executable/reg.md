{
  "date": "2021-08-02",
  "keywords": [
    "reg file",
    "reg file format",
    "what is a reg file",
    "file",
    "reg example",
    "reg file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about REG file format and APIs that can create and open REG files.",
  "title": "REG - Windows Registry File",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-reg"
    }
  },
  "lastmod": "2021-08-02"
}

## What is a REG file?

A REG file is simply a text file with the .reg extension. These files are usually created by exporting typical keys from the Registry. These files can also be used as a backup of the registry (Specially this step is important before making changes!). You can see that some made them available as downloadable files on the same sites that show you how to perform a Registry hack. A REG file is useful in making manual changes to the Registry and export those changes. Just clean up the file a bit and then share it with others.

## REG file format

The REG file format was designed for exporting and importing portions of the Windows registry using a INI-based syntax. The Windows Registry is a relational or hierarchical database that keeps the low-level settings for the Microsoft Windows operating system and other applications that use the Windows registry. Alternativley, we can say, the registry or Windows Registry consists of information, options, settings and other values for programs and hardware installed on all versions of Microsoft Windows operating systems.

### Syntax of REG file
Here are some key elements as the part of a REG file syntax:
- **RegistryEditorVersion**: E.g. "Windows Registry Editor Version 5.00" for Windows 2000, Windows XP, and Windows Server 2003.
- **Blank line**: Identifies the start of a new registry path.
- **RegistryPathx**: The path of the subkey that holds the first value you are importing.
- **DataItemNamex**: The name of the data item that you want to import.
- **DataTypex**: The data type for the registry value.

Keys are stored in .reg files using the following syntax:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
You can edit the Default Value of a key by using "@" instead of "Value Name":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Example

Here is an example of REG file
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## References

* [Windows Registry- by Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [How to add, modify, or delete registry subkeys and values by using a .reg file](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
