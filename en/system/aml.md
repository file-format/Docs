{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AML File - ACPI Machine Language File",
  "description":"Learn about ACPI AML file format and APIs that can create and open AML files.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
    }
  },
  "lastmod" : "2022-04-12"
}

## What is an AML file?

An AML file is a system file created with the Advanced Configuration and Power Interface (ACPI) language used for configuring hardware properties. It contains machine independent byte code that is used to configure hardware even for simple operations such as shutting down a computer. AML files may contain instructions depending on the purpose for which it is to be installed on the machine. Implementation of the ACPI standards lets you enhance power management functionality and a robust interface for configuring motherboard devices such as the P55 motherboards.

## ACPI AML File Format

AML files are saved as binary files to disc with contents written in byte code. The file format specifications of ACPI standard are available on [uefi](https://uefi.org/node/735). The language has been designed to offer stability and backward-compatibility, requiring less re-writes or re-builds of the application stack.

## AML File Format Specifications

An AML file comprises of DSDT and SSDT tables. The AML byte code is read and parsed from the beginning of each of these tables. This gives information about the definitions of devices and objects in the ACPI namespace. Using this information, the AML interpreter can generate a list of all devices available in the system, and their supported properties and functions.

### Example ASL Code for a DSDT

An example of ASL code for a DSDT is as following.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
        }
    }
}
```

## References

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)
