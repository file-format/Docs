{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ADM File - Administrative Template File Format",
  "description":"Learn about ADM file format and how to open ADM files.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
    }
  },
  "lastmod" : "2023-02-14"
}

## What is an ADM file?

An ADM file is a template file used by Microsoft Group Policies software to specify the location of registry-based policy settings in the registry file. It is used by system administrators to define the policy for managing a group of computers that are part of the group. This information becomes part of the Group Policy Objects (GPOs) that are created for management of the group.

You can open ADM files using Microsoft Group Policy Object Editor.

## ADM File Format - More Information

ADM files are stored as unicode-formatted text files. These were primarily used to desc the location of registry-based policy settings in Windows Vista and Windows 7 registry.

ADM files are no more supported and have been replaced by the [ADMX](/system/admx/) files. GPA ignores the following default ADM files on computers running Microsoft Windows Vista Service Pack 1 or later.

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## References

* [Administrative Template Files - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Managing Administrative Template Files](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)
