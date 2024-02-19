{
  "date": "2021-02-01",
  "keywords": [
    "usd",
    "usd file",
    "usd file format",
    "file format",
    "file",
    "extension",
    "3d"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "USD - সর্বজনীন দৃশ্য বর্ণনা বিন্যাস",
  "description": "USD ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা USD ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-bn"
    }
  },
  "lastmod": "2021-02-01"
}

## একটি USD ফাইল কি?

.usd এক্সটেনশন সহ একটি ফাইল হল একটি সর্বজনীন দৃশ্য বর্ণনা ফাইল বিন্যাস যা ডিজিটাল সামগ্রী তৈরির অ্যাপ্লিকেশনগুলির মধ্যে ডেটা আদান-প্রদান এবং বৃদ্ধির উদ্দেশ্যে ডেটা এনকোড করে৷ Pixar দ্বারা বিকাশিত, [USD](https://openusd.org/release/intro.html) মৌলিক সম্পদ (যেমন মডেল) বা অ্যানিমেশন বিনিময় করার ক্ষমতা প্রদান করে।

## USD ফাইল ফরম্যাট

USD ফাইলের বাইনারি ফরম্যাট (ক্রেট ফাইল নামেও পরিচিত) বা ASCII-ব্যাকড ফাইল থাকতে পারে। এই উভয় ফাইল ফরম্যাটই বিনিময়যোগ্য যেখানে তথ্যসূত্রগুলিকে উৎস পরিবর্তন না করে .usd সম্পদের সাথে লিঙ্ক করা যেতে পারে। USD ফাইল বিন্যাসে স্ক্রিপ্টিংয়ের জন্য Python বাইন্ডিং সহ C++ লাইব্রেরির একটি সেট থাকে। এটি যেকোন সংখ্যক 3D দৃশ্য উপাদান যেমন ভার্চুয়াল সেট, দৃশ্য এবং শটগুলিকে অ্যাপ্লিকেশন থেকে অ্যাপ্লিকেশনে প্রেরণ করতে সমাবেশ এবং সংগঠনকে সক্ষম করে।

### USD ডেটা প্রকার

USD ফাইল ফরম্যাট দ্বারা সমর্থিত মৌলিক ডেটা প্রকারগুলি নিম্নলিখিত সারণীতে তালিকাভুক্ত করা হয়েছে।

|মান প্রকার টোকেন |C++ প্রকার |বিবরণ |
---|---|---|
|বুল|বুল||
|uchar|uint8_t|8 বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা|
|int|int32_t|32 বিট স্বাক্ষরিত পূর্ণসংখ্যা|
|uint|uint32_t|32 বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা|
|int64|int64_t|64 বিট স্বাক্ষরিত পূর্ণসংখ্যা|
|uint64|uint64_t|64 বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা|
|অর্ধেক|GfHalf|16 বিট ফ্লোটিং পয়েন্ট|
|float|float|32 bit floating point|
|ডাবল|ডাবল|64 বিট ফ্লোটিং পয়েন্ট|
|timecode|SdfTimeCode|একটি সমাধানযোগ্য সময়ের প্রতিনিধিত্ব করে দ্বিগুণ|
|string|std::string|stl স্ট্রিং|
|টোকেন|TfToken|দ্রুত তুলনা এবং হ্যাশিং সহ ইন্টার্নড স্ট্রিং|
|সম্পদ|SdfAssetPath|অন্য সম্পদে একটি সমাধানযোগ্য পথ উপস্থাপন করে|
|matrix2d|GfMatrix2d|2x2 ম্যাট্রিক্স অফ ডাবলস|
|matrix3d|GfMatrix3d|3x3 ম্যাট্রিক্স অফ ডাবলস|
|matrix4d|GfMatrix4d|4x4 ম্যাট্রিক্স অফ ডাবলস|
|quatd|GfQuatd|ডাবল-নির্ভুল চতুর্ভুজ|
|quatf|GfQuatf|একক-নির্ভুল quaternion|
|quath|GfQuath|অর্ধ-নির্ভুল quaternion|
|double2|GfVec2d|2 ডাবলের ভেক্টর|
|float2|GfVec2f|2টি ফ্লোটের ভেক্টর|
|হাফ2|GfVec2h|2 অর্ধের ভেক্টর|
|int2|GfVec2i|2 ints এর ভেক্টর|
|ডাবল3|GfVec3d|3 ডাবলের ভেক্টর|
|float3|GfVec3f|3টি ফ্লোটের ভেক্টর|
|অর্ধেক|GfVec3h|3 অর্ধের ভেক্টর|
|int3|GfVec3i|3 ints এর ভেক্টর|
|double4|GfVec4d|4 ডাবলের ভেক্টর|
|float4|GfVec4f|4টি ফ্লোটের ভেক্টর|
|হাফ4|GfVec4h|4 অর্ধেক এর ভেক্টর|
|int4|GfVec4i|4 ints এর ভেক্টর|

## USD উদাহরণ

প্লেইন ASCII ফাইল ফরম্যাটে একটি USD ফাইলের উদাহরণ নিম্নরূপ।

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## তথ্যসূত্র ##

* [ইউএসডির ভূমিকা](https://openusd.org/release/intro.html)

* [USD API রেফারেন্স](https://openusd.org/release/apiDocs.html)


