{
  "date" : "2020-08-20",
  "keywords" : [ "eot file", "eot file format", "what is a eot file", "file", "eot example", "eot file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EOT - TrueType Font File Format",
  "description":"Learn about EOT File Format and APIs to create and open EOT files.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-10-21"
}

## What is an EOT file?

A file with .eot extension is an OpenType font that is embedded in a document. These are mostly used in web files such as a Web page. It was created by Microsoft and is supported by Microsoft Products including PowerPoint presentation [.pps](/presentation/pps) file. The file isn't of primary use and is sort of accompanying document with the main document or web page. Similar to OTF fonts, EOT supports both Postscript and TrueType outlines for the glyphs. EOT files are smaller in size for the reason that they are compressed using LZ compression. EOT uses a Microsoft tool to create a font from existing TTF/OTF fonts.

## Brief History

The EOT font was submitted to W3C in 2007 as part of CSS3 but due to its requirements to be permanently installed on remote system became the reason of its rejection. It was resubmitted in March 2008, but W3C ultimately chose [Web Font Format](/font/woff/) (WOFF) which was standardized then.

## EOT File Format

EOT file format details can be found on [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat) and elaborates the structure used by this font format. The EOT consists of a single EMBEDDEDFONT structure that provides enough basic information about hte font name and supported characters. The packing of this information lets User Agents to avoid unpacking, decompressing or installing the font if it is already present on the machine.

### EMBEDDEDFONT Structure
The EMBEDDEDFONT structure has underwent three revisions, with addition of additional data at the end of the structure with each revision. The last revision of the EMBEDDEDFONT structure is as depicted below.

|Data Type|Entry Name|Description|
---|---|---|
|unsigned long|EOTSize|Total structure length in bytes (including string and font data)|
|unsigned long|FontDataSize|Length of the OpenType font (FontData) in bytes|
|unsigned long|Version|Version number of this format - 0x00020002|
|unsigned long|Flags|Processing Flags|
|byte[10]|FontPANOSE|The PANOSE value for this font - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|In Windows this is derived from TEXTMETRIC.tmCharSet. This value specifies the character set of the font. DEFAULT_CHARSET (0x01) indicates no preference. - See https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|If the bit for ITALIC is set in OS/2.fsSelection, the value will be 0x01 - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|The weight value for this font - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Type flags that provide information about embedding permissions - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Magic number for EOT file - 0x504C. Used to check for data corruption.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63) - See https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - See https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - must be 0|
|unsigned long|Reserved2|Reserved - must be 0|
|unsigned long|Reserved3|Reserved - must be 0|
|unsigned long|Reserved4|Reserved - must be 0|
|unsigned short|Padding1|Padding to maintain long alignment. Padding value must always be set to 0x0000.|
|unsigned short|FamilyNameSize|Number of bytes used by the FamilyName array|
|byte|FamilyName[FamilyNameSize]|Array of UTF-16 characters the length of FamilyNameSize bytes. This is the English language Font Family string found in the name table of the font (name ID = 1) - See https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Padding value must always be set to 0x0000.|
|unsigned short|StyleNameSize|Number of bytes used by the StyleName|
|byte|StyleName[StyleNameSize]|Array of UTF-16 characters the length of StyleNameSize bytes. This is the English language Font Subfamily string found in the name table of the font (name ID = 2) - See https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Padding value must always be set to 0x0000.|
|unsigned short|VersionNameSize|Number of bytes used by the VersionName|
|bytes|VersionName[VersionNameSize]|Array of UTF-16 characters the length of VersionNameSize bytes. This is the English language version string found in the name table of the font (name ID = 5) - See https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Padding value must always be set to 0x0000.|
|unsigned short|FullNameSize|Number of bytes used by the FullName|
|byte|FullName[FullNameSize]|Array of UTF-16 characters the length of FullNameSize bytes. This is the English language full name string found in the name table of the font (name ID = 4) - See https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Padding value must always be set to 0x0000.|
|unsigned short|RootStringSize|Number of bytes used by the RootString array|
|byte|RootString[RootStringSize]|Array of UTF-16 characters the length of RootStringSize bytes.|
|unsigned long|RootStringCheckSum|RootString CheckSum value. See algorithm to process RootStringChecksum below.|
|unsigned long|EUDCCodePage|Codepage value needed for EUDC font support.|
|unsigned short|Padding6|Padding value must always be set to 0x0000.|
|unsigned short|SignatureSize|Number of bytes used by the Signature array. Currently reserved and should be set to 0x0000.|
|byte|Signature[SignatureSize]|Currently reserved. If the SignatureSize is 0x0000 there is no length to this array.|
|unsigned long|EUDCFlags|Processing flags for the EUDC font. Typical values might be TTEMBED_XORENCRYPTDATA and TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Number of bytes used by the Signature array.|
|byte|EUDCFontData[EUDCFontSize]|Number of bytes used for the EUDC font data. If the EUDCFontSize is 0x00000000 there is no length to this array.|
|byte|FontData[FontDataSize]|The font data for this EOT file. The data may be compressed or XOR encrypted as indicated by the processing flags.|

## References

 * [EOT File Format](https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Font Embedding](https://en.wikipedia.org/wiki/Font_embedding)
