{
  "date": "2019-10-11",
  "keywords": [
    "vcxproj",
    "file",
    "extension",
    "file format",
    "Visual C++ Project",
    "Programming Guide"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "VCXPROJ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা VCXPROJ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxproj-bn"
    }
  },
  "lastmod": "2020-09-10"
}

## একটি VCXPROJ ফাইল কি?

.vcxproj এক্সটেনশন সহ একটি ফাইল হল একটি Microsoft Visual C++ প্রকল্প ফাইল যা [C++](/programming/cpp/) প্রকল্পের তথ্য সংরক্ষণ করে। এটিতে এমন তথ্য রয়েছে যা MSBuild প্রকল্প সিস্টেম দ্বারা কম্পাইল এবং চূড়ান্ত আউটপুট তৈরি করতে ব্যবহৃত হয়। ভিজ্যুয়াল C++ প্রকল্পগুলির VCXPROJ .NET প্রকল্পগুলির জন্য [CSPROJ](/programming/csproj/) এর মতোই৷ VCXPROJ ফাইলগুলিতে কোনও কোড থাকে না তবে প্রকল্পটি নির্মাণের জন্য প্রকল্পের জন্য সংজ্ঞায়িত সমস্ত শ্রেণী, লক্ষ্য এবং বৈশিষ্ট্যগুলিকে বোঝায়। এগুলি প্লেইন টেক্সট এডিটরগুলিতে বা বিশেষত Microsoft ভিজ্যুয়াল স্টুডিও আইডিই-তে খোলা যেতে পারে।


## VCXPROJ ফাইল ফরম্যাট - আরও তথ্য

VCXPROJ ফাইলগুলি হল পাঠ্য ফাইল যা [XML](/web/xml/) ফাইল বিন্যাসে তৈরি করা হয়৷ এগুলি যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে তবে এই ফাইলগুলি খোলার এবং সম্পাদনা করার জন্য মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও আইডিই ব্যবহার করার জন্য অত্যন্ত সুপারিশ করা হয়। এগুলি ম্যানুয়াল সম্পাদনার জন্য ডিজাইন করা হয়নি। ভুলের কারণে IDE ক্র্যাশ হতে পারে বা অপ্রত্যাশিত উপায়ে আচরণ করতে পারে।

একটি নমুনা VCXPROJ ফাইলের বিষয়বস্তু নিম্নরূপ।

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ ফাইল উপাদান

একটি সাধারণ VCXPROJ ফাইলে অনেকগুলি উপাদান থাকে যা উপরের XML উদাহরণে দেখা যায়। মাইক্রোসফ্টের [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) প্রতিটি ফাইল উপাদানের বিস্তারিত ব্যাখ্যা করে এবং বিকাশকারীর দৃষ্টিকোণ থেকে উল্লেখ করা যেতে পারে।

#### প্রকল্পের উপাদান

এটি VCXPROJ ফাইলের রুট নোড। MSBuild বিল্ড সংস্করণ এবং সংকলনের জন্য ডিফল্ট লক্ষ্য পড়তে এই উপাদানটি ব্যবহার করে।

#### প্রজেক্ট কনফিগারেশন আইটেমগ্রুপ এলিমেন্ট

এটিতে প্রোজেক্ট কনফিগারেশন তথ্য রয়েছে যা বিল্ড পদ্ধতি (ডিবাগ বা রিলিজ), 32 বা 64-বিট সংকলন, অপ্টিমাইজেশন বিকল্প এবং অন্যান্য অন্তর্ভুক্ত করতে পারে। এই গ্রুপের তথ্য IDE দ্বারা প্রকল্প লোড করার জন্য ব্যবহার করা হয়।

#### প্রজেক্ট কনফিগারেশন উপাদান

একটি VCXPROJ ফাইলের প্রজেক্ট কনফিগারেশন উপাদানগুলিতে বিল্ড এবং প্ল্যাটফর্ম সম্পর্কে তথ্য রয়েছে যার জন্য প্রকল্পটি লোড করা হয়েছে। এর নামটি `$(কনফিগারেশন)|$(প্ল্যাটফর্ম)' ফরম্যাট অনুসরণ করা উচিত।

#### গ্লোবাল প্রপার্টি গ্রুপ এলিমেন্ট

এই বিভাগে সেটিংস রয়েছে যা প্রকল্প স্তরের জন্য তথ্য প্রদান করে যেমন:

 * প্রজেক্টগুইড
 * রুট নেমস্পেস
 * ApplicationType বা ApplicationTypeRevision


## তথ্যসূত্র

* [VCXPROJ স্ট্রাকচার - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ প্রকল্প ফাইল](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


