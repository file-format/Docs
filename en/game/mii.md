{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about Age of Empires 2 Expansion Replay MGX file format and APIs that can create and open MGX files.",
  "title" : "MII File - Wii Virtual Avatar File Format",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
    }
  },
  "lastmod" : "2023-01-15"
}

## What is a MII file?

A MII file is a virtual avatar file format used to store virtual avatars on the Nintendo Wii gaming console. These files contain information such as the avatar's appearance, movements, and animations. They can be used in games, social networking applications, and other software on the Wii. A MII file also contains other features about the avatar such as the gender, hair color, skin color, facial features, and eye type.

You can open a MII file using the [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII File Format

The MII file format is defined in detail on [Wii Brew](https://wiibrew.org/wiki/Mii_data). Strings in a MII file are stored in Unicode format (UTF-16), big-endian.

### MI Block

MII file data is stored on the Wiimote in two blocks. Each block is 750 bytes in length, with 2 byte CRC, making it a total of 752 bytes. Each block starts with a 4-byte value ('RNCD') that seems to be the magical number for the MII file format.

## How to Create MII Files?

There are a few different ways to create avatars for the Nintendo Wii:

1. `Using the built-in Mii channel on the Wii:` This channel allows you to create custom avatars using a variety of tools, including facial features, body shape, and clothing. Once you've created your avatar, you can save it as a Mii file and use it in games and other software on the Wii.

1. `Using the Mii Maker app on the Nintendo 3DS:` The Mii Maker app allows you to create custom avatars using the touch screen and camera on your Nintendo 3DS. Once you've created your avatar, you can save it as a Mii file and transfer it to your Wii via a wireless connection.

1. `Using third-party software:` Some developers have created software that allows you to create custom avatars for the Wii. This software is typically designed for use on a computer and may require additional steps to transfer the avatar to your Wii.

1. `Using pre-made avatars:` Some games and other software on the Wii may come with pre-made avatars that you can use.

In all cases, you need to have a Nintendo account to create and save your avatar on the Wii.

## References

* [My Avatar Editor](https://rc24.xyz/goodies/mii/)
* [Wii Brew](https://wiibrew.org/wiki/Mii_data)
