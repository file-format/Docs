{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NPK File Format",
  "description":"Learn about NPK file format and APIs that can create and open NPK files.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk-az",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## What is an NPK file?

An NPK file is a software upgrade package file used by **MikroTik** routers for upgrade of router operating system. It comes as a compressed binary archive that is loaded in the router for installing software updates. Information contained inside an NPK files include networking information such as IP address and IP service, connectors information (ethernet interfaces and serial port), email setup, bridge configuration, and local user management.

## NPK File Format

NPK files are stored as compressed binary archive. It is a closed file format that is used by MikroTik themselves only. It is not intended to create RouterOS add-ons via 3rd parties. NPK files are maintained by MikroTik itself and upgraded versions of the same can be downloaded from the download sections of [MikroTik](https://mikrotik.com/download) website.

When an NPK file is uploaded to a router, the router OS doesn't come in effect unless it is rebooted. Therefore, a restart is required in order for the router OS to be upgraded.

## References

* [MikroTik - Upgrading Router OS](https://mikrotik.com/download)

* [How to Create NPK Files](https://forum.mikrotik.com/viewtopic.php?t=87126)


