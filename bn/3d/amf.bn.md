{
  "date": "2019-10-11",
  "keywords": [
    "amf",
    "amf file",
    "amf file format",
    "file format",
    "3d"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "AMF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা AMF ফাইল খুলতে এবং তৈরি করতে পারে।",
  "title": "AMF - অ্যাডেটিভ ম্যানুফ্যাকচারিং ফাইল",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-amf-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি AMF ফাইল কি?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF ফাইল ফরম্যাট

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### একটি AMF ফাইলের উপাদান

এর সাথে সংজ্ঞায়িত পাঁচটি শীর্ষ স্তরের উপাদান<AMF> ট্যাগ নিচে বিস্তারিত হিসাবে আছে. একটি সম্পূর্ণ কার্যকরী AMF ফাইলের জন্য একটি একক বস্তু উপাদানের উপস্থিতি আবশ্যক।

`<object> ` - বস্তু উপাদান একটি ভলিউম বা উপাদানের ভলিউম সংজ্ঞায়িত করে, যার প্রত্যেকটি মুদ্রণের জন্য একটি উপাদান আইডির সাথে যুক্ত। ফাইলটিতে অন্তত একটি বস্তুর উপাদান থাকতে হবে। অতিরিক্ত বস্তু ঐচ্ছিক.

`<material> ` - ঐচ্ছিক উপাদান উপাদান একটি সংশ্লিষ্ট উপাদান ID দিয়ে মুদ্রণের জন্য এক বা একাধিক উপকরণ সংজ্ঞায়িত করে। কোন উপাদান উপাদান অন্তর্ভুক্ত না হলে, একটি একক ডিফল্ট উপাদান অনুমান করা হয়.

`<texture> ` - ঐচ্ছিক টেক্সচার উপাদান রঙ বা টেক্সচার ম্যাপিংয়ের জন্য এক বা একাধিক ছবি বা টেক্সচারকে সংজ্ঞায়িত করে, প্রতিটি একটি সংশ্লিষ্ট টেক্সচার আইডি সহ।

`<constellation> ` - ঐচ্ছিক নক্ষত্রমণ্ডল উপাদানটি শ্রেণিবদ্ধভাবে বস্তু এবং অন্যান্য নক্ষত্রপুঞ্জকে মুদ্রণের জন্য একটি আপেক্ষিক প্যাটার্নে একত্রিত করে।

`<metadata> ` - ঐচ্ছিক মেটাডেটা উপাদান ফাইলে থাকা বস্তু(গুলি) এবং উপাদান সম্পর্কে অতিরিক্ত তথ্য নির্দিষ্ট করে।

## AMF উদাহরণ

নিম্নলিখিত AMF ফাইলের একটি উদাহরণ যা একটি [text](/word-processing/txt/) ফাইলে অনুলিপি করা যেতে পারে এবং খোলার জন্য সংকুচিত [zip](/compression/zip/) ফাইল হিসাবে সংরক্ষণ করা যেতে পারে৷
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## তথ্যসূত্র

 * [AMF - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [ISO-তে AMF স্পেসিফিকেশন](https://www.iso.org/standard/67472.html)

