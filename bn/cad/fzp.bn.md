{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "FZP ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা FZP ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "FZP ফাইল ফরম্যাট - Fritzing XML অংশ বর্ণনা ফাইল",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## একটি FZP ফাইল কি?

একটি FZP ফাইল হল একটি XML ফাইল যা [Fritzing](https://fritzing.org/) ইলেকট্রনিক সার্কিট প্রোটোটাইপিং এবং ডিজাইন অ্যাপ্লিকেশন দ্বারা তৈরি করা হয়েছে। এতে অংশের বৈশিষ্ট্য, সংযোগকারী এবং বাস সম্পর্কে তথ্য রয়েছে [XML](/web/xml/) ফাইল ফরম্যাটে। FPZ ফাইল Fritzing স্বাধীনভাবে ব্যবহার করা যাবে না. পরিবর্তে, সেগুলি FZPZ সংরক্ষণাগার ফাইলের অংশ হিসাবে আমদানি করা হয়৷

## FZP ফাইল ফরম্যাট - আরও তথ্য

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## FZP ফাইল স্ট্রাকচারের উদাহরণ

একটি সাধারণ FZP ফাইলের নিম্নলিখিত XML গঠন রয়েছে।

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## তথ্যসূত্র

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [fzpz এক্সটেনশন সহ নতুন অংশ](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


