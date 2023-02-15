{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ADMX File - Group Policy Administrative Template File Format",
  "description":"Learn about ADMX file format and how to open ADMX files.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
    }
  },
  "lastmod" : "2023-02-14"
}

## What is an ADMX file?

An ADMX file is a policy configuration file used by Microsoft Windows Group Policy software that manages group of computers in a group. It is an XML-based administrative template file and was introduced with Windows Vista Service Pack 1. ADMX files contain configuration settings for user accounts, operating system configurations, and applications. ADMX files are used to store and deploy the configurations for the centralised management of many computer systems.

You can create or edit ADMX files using any XML-compatible, any text editor or Microsoft Group Policy Object Editor.

## ADMX File Format - More Information

ADMX files are stored in the universal [XML](/web/xml/) file format that is human-readable. It is multilingual file format and allows system administrators from different languages to work with the same ADMX files. ADMX files replaced the old [ADM](/system/adm/) file format which is a unicode‑formatted text file format. ADMX files specify the registry keys that are changed when a certain Group Policy setting is changed.

### What can I do with ADMX file?

ADMX files define what actions are to be allowed to user computers that are part of a group. The group policy imposes the rules set in combination with Active Directory software. ADMX files are managed from the central store on Windows OS that is a central location in the domain.

An ADMX file deployed in a working environment can let administrators implement policies such as:

 * Control the use of internet
 * Downloading of certain types of files
 * Use of removable devices on the systems

## References

* [Administrative Template Files - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Managing Administrative Template Files](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)
