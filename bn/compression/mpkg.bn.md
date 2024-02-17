{
  "date" : "2019-10-11",
  "keywords" : [ "mpkg file", "mpkg file format", "what is a mpkg file", "file", "mpkg example", "mpkg file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPKG ফাইল ফরম্যাট - মেটা প্যাকেজ ফাইল",
  "description":"MPKG ফাইল ফরম্যাট এবং APIগুলি সম্পর্কে জানুন যা MPKG ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## একটি MPKG ফাইল কি?

.mpkg এক্সটেনশন সহ একটি ফাইল হল একটি সংরক্ষণাগার ইনস্টলার ফাইল, যা বেশিরভাগই MacOS অপারেটিং সিস্টেমে পাওয়া যায়। এটিতে অ্যাপ্লিকেশনটির সমস্ত প্রয়োজনীয় ইনস্টলেশন ফাইল রয়েছে যা সংশ্লিষ্ট ফাইলগুলিকে আলাদাভাবে রাখার প্রয়োজন ছাড়াই। একটি একক MPKG ফাইলে অন্যান্য ফাইল ছাড়াও ইনস্টলেশন ফাইলগুলির একটি হিসাবে প্যাকেজ ফাইল [PKG](/compression/pkg/) থাকতে পারে৷ MPKG ফাইলগুলি কোনো সাধারণ সফ্টওয়্যার দিয়ে খোলা যায় না এবং Apple Installer ব্যবহার করে MacOS-এ স্বয়ংক্রিয়ভাবে কার্যকর হয়।

## MPKG ফাইল ফরম্যাট

একটি MPKG ফাইলে বিভিন্ন ধরনের ফাইল থাকে যা এটিতে থাকা একাধিক প্যাকেজ ইনস্টল করার জন্য প্রয়োজনীয়। এটি নীচের চিত্র থেকে দেখা যায় যা একটি নমুনা MPKG ফাইলের গাছের গঠন। এই গাছের কাঠামোটি MacOS টার্মিনালে `tree` কমান্ড ব্যবহার করে রপ্তানি করা হয়।

{{< figure src="../mpkg.png" alt="MPKG ফাইল ফরম্যাট" >}}

The description of different elements in the image is as follow.

প্যাকেজ ডিরেক্টরি' - pkg ফাইলগুলির একটি তালিকা সংরক্ষণ করে, অর্থাৎ, সাব-প্যাকেজের একটি তালিকা
`রিসোর্স ডিরেক্টরি` - pkg দ্বারা ব্যবহৃত সম্পদ সঞ্চয় করে, যেমন স্থানীয়কৃত রিসোর্স এবং ছবি, Rtf ডকুমেন্ট, pdf ডকুমেন্ট ইত্যাদি।
`Distribution.dist ফাইল` - একটি xml ডকুমেন্ট যেখানে তথ্য রয়েছে যেমন ইনস্টল করা সাব-প্যাকেজ এবং রানটাইম স্ক্রিপ্ট

একটি MPKG ফাইলের জন্য নমুনা XML ফাইল সংশ্লিষ্ট সাব-প্যাকেজের উপর নির্ভর করে অনুসরণ করতে পারে।

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - ইনস্টল করা সাব-প্যাকেজ। এটি pkg বিন্যাসে বান্ডেল কাঠামোর একটি ডিরেক্টরি। এটিতে একটি বিষয়বস্তু উপ-ডিরেক্টরি রয়েছে।

## তথ্যসূত্র

* [OSX ফ্ল্যাট প্যাকেজ](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG প্যাকেজ ম্যানেজার](https://github.com/puellavulnerata/mpkg)


