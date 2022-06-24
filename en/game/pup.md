{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PUP File Format - PlayStation 3 Update File",
  "description":"Learn about PUP file format and APIs that can create and open PUP files.",
  "linktitle" : "PUP",
  "menu" : {
    "docs" : {
      "identifier":"game-pup",
      "parent" : "game"
    }
  },
  "lastmod" : "2022-06-23"
}

## What is a PUP file?

A PUP file is a system update patch file used by PlayStation 4 (PS4) and PlayStation 5 (PS5) system software. It upgrades the game's firmware to a newer version that may contain software enhancements in terms of bug fixes, new operating system features, and improvements in terms of software performance. The PUP file may also contain patches to fix bugs that can otherwise result in security issues. PUP files can be downloaded to the system by connecting it to internet or manually downloading the firmware update to a computer and then transferring to the  device using a USB stick or another storage device. The earlier version of PlayStation i.e. PS3 also used the PUP file for upgrade of firmware.

## PUP File Format - More Information

PUP files are saved to disc in [compressed](/compression/) binary file format. However, the details of compression are not available publicly. The contents of a PUP file can be extracted using the PS3 PUP Extractor program on Windows OS. In order to upgrade the software system of PS3, the PUP file is uploaded and saved to the /PS3/UPDATE folder on the machine. This lets the system update option find the firmware upgrade file and run it.

### PUP File Format Naming Convention

 * `PS3UPDAT.PUP` - The standard filename used for PlayStation 3 updates
 * `PS4UPDATE.PUP` - The standard filename used for PlayStation 4 updates
 * `PS5UPDATE.PUP` - The standard filename used for PlayStation 5 updates

## Using PUP File to Factory Reset PlayStation

PUP files can be used to factory reset your PlayStation device. This will overwrite all the data from the device, remove the existing firmware and set it as a brand new device. Factory resetting your PlayStation will also remove any saved game data.

## References

 * [PS3 System Software Update](https://www.playstation.com/en-us/support/hardware/ps3/system-software/)
