{
  "date" : "2021-02-20",
  "keywords" : [ "WMA", "file", "extension", "format", "audio interchange file format", "music" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "WMA ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি WMA ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "WMA - উইন্ডোজ মিডিয়া অডিও ফাইল",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## একটি WMA ফাইল কি?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. অডিও বিষয়বস্তু ছাড়াও, একটি WMA ফাইলে মেটাডেটা অবজেক্টও থাকে যেমন শিরোনাম, অ্যালবাম, শিল্পী এবং ট্র্যাকের জেনার। WMA ফাইলগুলি প্রাথমিকভাবে [.mp3](/audio/mp3/) ফাইলগুলির মতো ওয়েবে স্ট্রিমিংয়ের জন্য ব্যবহৃত হয়৷

## WMA ফাইল ফরম্যাট

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. যাইহোক, ডিইসিই আল্ট্রাভায়োলেট এবং এমপিইজি-ড্যাশ-এর মতো সংশ্লিষ্ট শিল্প মানদণ্ড দ্বারা এটিকে প্রমিত অডিও কোডেক হিসাবে ঘোষণা করা হয়নি।

### WMA টাইপ নির্দিষ্ট ডেটা

উইন্ডোজ মিডিয়া অডিও কোডেক-এর জন্য টাইপ-নির্দিষ্ট তথ্য স্ট্রিম প্রোপার্টিজ অবজেক্টের টাইপ-নির্দিষ্ট ডেটার অংশ হিসাবে নিম্নলিখিত বিন্যাসে সংরক্ষণ করা হয়।

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## তথ্যসূত্র

* [ASF ওভারভিউ - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


