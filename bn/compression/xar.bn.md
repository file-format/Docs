{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - এক্সটেনসিবল আর্কাইভ ফাইল ফরম্যাট",
  "description":"XAR ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি XAR ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-bn",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## একটি XAR ফাইল কি?

.xar (এক্সটেনসিবল আর্কাইভ ফরম্যাট) এক্সটেনশন সহ একটি ফাইল হল একটি UNIX আর্কাইভ যা সংকুচিত বা নন-কম্প্রেস ফরম্যাটে হতে পারে। এটি প্যাকেজ ইনস্টল করার জন্য Mac OS এও ব্যবহৃত হয়। XAR হল ওপেন সোর্স এবং Safari ব্রাউজারের সাথে ব্যবহারের জন্য Mac OS X 10.5 এর অংশ।

## XAR ফাইল ফরম্যাট

একটি [XAR](https://github.com/mackyle/xar/wiki/xarformat) ফাইলের তিনটি প্রধান অঞ্চল রয়েছে৷

 * হেডার
 * সুচিপত্র
 * গাদা

### XAR হেডার

XAR শিরোনামটি নিম্নরূপ গঠন করা হয়েছে।

|ক্ষেত্র|ডেটা টাইপ|বাইটে আকার|
---|---|---|
|ম্যাজিক|আনসাইনড int 32|4|
|আকার
|সংস্করণ | স্বাক্ষরবিহীন int 16|2|
|TOC দৈর্ঘ্য সংকুচিত| স্বাক্ষরবিহীন int 64|8|
|TOC দৈর্ঘ্য আনকমপ্রেসড|আনসাইনড ইনট 64|8|
|চেকসাম|আনসাইনড ইন্টি 32|4|
|মেসেজ ডাইজেস্টের নাম |শূন্য শেষ||৷

XAR হেডারের C স্ট্রাকচারকে অনুসরণ করে সংজ্ঞায়িত করা যেতে পারে।
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
মনে রাখবেন যে হেডারের সমস্ত ক্ষেত্র (জাদু, আকার, সংস্করণ, toc_length_compressed, toc_length_uncompressed, cksum_alg) সর্বদা নেটওয়ার্ক বাইট (ওরফে বড় এন্ডিয়ান) ক্রমে XAR ফাইলগুলিতে সংরক্ষণ করা হয়।

### XAR বিষয়বস্তুর সারণী (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. এটি ফাইলের শুরুতে সংরক্ষণ করা হয়, যার ফলে আর্কাইভের মাধ্যমে স্ক্যান করা সহজ হয় যাতে পৃথক ফাইল বের করা যায়। XAR আর্কাইভ আপনাকে বিভিন্ন কম্প্রেশন স্কিম যেমন [GZIP](/compression/gz/), [BZIP2](/compression/bz2/), এবং অন্যান্য অনুরূপ ব্যবহার করে স্বতন্ত্রভাবে আর্কাইভের পৃথক ফাইলগুলিকে সংকুচিত/এনকোড করতে দেয়।  

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### গাদা

কম্প্রেসড টকের পরপরই হিপ শুরু হয়। এটি TOC দ্বারা উল্লেখ করা ডেটার একটি অসংগঠিত স্তূপ। TOC-তে তালিকাভুক্ত অফসেট মানগুলি হিপের শুরু থেকে শুরু হয়। toc-এর দৈর্ঘ্যের মানগুলি হিপে সংরক্ষিত বাইটের প্রকৃত সংখ্যাকে নির্দেশ করে (সংকুচিত বা না) যেখানে আকারের মান আইটেমের নিষ্কাশিত আকারকে নির্দেশ করে (প্রয়োজনে ডিকম্প্রেস করার পরে)।

## তথ্যসূত্র

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Xar_(archiver))


