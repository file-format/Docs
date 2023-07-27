{
  "date" : "2019-10-11",
  "keywords" : [ "tgs file", "tgs file format", "what is a tgs file", "file", "tgs example", "tgs file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TGS - Telegram Animated Sticker File Format",
  "description":"Learn about TGS file format and APIs that can create and open TGS files.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-02"
}

## What is a TGS file?

A file with .tgs extension is an animated sticker file that was introduced by the cross-platform messaging service, [Telegram](https://core.telegram.org/stickers#animated-stickers). Animated stickers are used by messaging apps users to send more enhanced and lively content in messages unlike the static graphics that are still images. Telegram initially used the [WEBP](/image/webp/) file format for still image stickers. The TGS file format can store animation data at higher resolutions and smaller file size as compared to the static WEBP stickers. TGS files can be opened using applications such as Telegram, 7-zip, Apple Archive Utility, and Corel WinZip.

## TGS File Format

Telegram introduced the TGS file format back in July 2019 based on the Lottie library. A TGS file consists of [JSON](/web/json/) text that is exported from an animation in Adobe After Effects. The exported JSON text is compressed using the gzip compression which reduces the file size. The JSON information about the text file is stored in text file that becomes the basis of high compression rates.

### TGS Stickers Specifications

The TGS file format imposes certain limitations on the TGS animated stickers creation. A TGS animated file:

 * Sticker/canvas size must be 512х512 pixels.
 * Sticker objects must not leave the canvas.
 * Animation length must not exceed 3 seconds.
 * All animations must be looped.
 * Sticker size must not exceed 64 KB after rendering in Bodymovin.
 * All animations must run at 60 Frames Per Second.

### Sample TGS JSON Text

A sample animated sticker, when unzipped, contains the following JSON text content.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## References ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
