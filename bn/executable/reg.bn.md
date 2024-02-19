{
  "date": "2021-08-02",
  "keywords": [
    "reg file",
    "reg file format",
    "what is a reg file",
    "file",
    "reg example",
    "reg file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "REG ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি REG ফাইল তৈরি এবং খুলতে পারে।",
  "title": "REG - উইন্ডোজ রেজিস্ট্রি ফাইল",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-reg-bn"
    }
  },
  "lastmod": "2021-08-02"
}

## একটি REG ফাইল কি?

একটি REG ফাইল হল .reg এক্সটেনশন সহ একটি পাঠ্য ফাইল। এই ফাইলগুলি সাধারণত রেজিস্ট্রি থেকে সাধারণ কী রপ্তানি করে তৈরি করা হয়। এই ফাইলগুলি রেজিস্ট্রির ব্যাকআপ হিসাবেও ব্যবহার করা যেতে পারে (বিশেষত পরিবর্তন করার আগে এই পদক্ষেপটি গুরুত্বপূর্ণ!) আপনি দেখতে পাচ্ছেন যে কেউ কেউ সেগুলিকে একই সাইটে ডাউনলোডযোগ্য ফাইল হিসাবে উপলব্ধ করেছে যা আপনাকে দেখায় কিভাবে একটি রেজিস্ট্রি হ্যাক করতে হয়। একটি REG ফাইল রেজিস্ট্রিতে ম্যানুয়াল পরিবর্তন করতে এবং সেই পরিবর্তনগুলি রপ্তানি করতে কার্যকর। ফাইলটি একটু পরিষ্কার করুন এবং তারপর অন্যদের সাথে শেয়ার করুন।

## REG ফাইল ফরম্যাট

REG ফাইল বিন্যাসটি INI-ভিত্তিক সিনট্যাক্স ব্যবহার করে উইন্ডোজ রেজিস্ট্রির অংশগুলি রপ্তানি এবং আমদানি করার জন্য ডিজাইন করা হয়েছিল। উইন্ডোজ রেজিস্ট্রি হল একটি রিলেশনাল বা হায়ারার্কিক্যাল ডাটাবেস যা মাইক্রোসফট উইন্ডোজ অপারেটিং সিস্টেম এবং উইন্ডোজ রেজিস্ট্রি ব্যবহার করে এমন অন্যান্য অ্যাপ্লিকেশনের জন্য নিম্ন-স্তরের সেটিংস রাখে। অল্টারনেটিভলি, আমরা বলতে পারি, রেজিস্ট্রি বা উইন্ডোজ রেজিস্ট্রি মাইক্রোসফ্ট উইন্ডোজ অপারেটিং সিস্টেমের সমস্ত সংস্করণে ইনস্টল করা প্রোগ্রাম এবং হার্ডওয়্যারের জন্য তথ্য, বিকল্প, সেটিংস এবং অন্যান্য মান নিয়ে গঠিত।

### REG ফাইলের সিনট্যাক্স
এখানে একটি REG ফাইল সিনট্যাক্সের অংশ হিসাবে কিছু মূল উপাদান রয়েছে:
- **RegistryEditorVersion**: যেমন Windows 2000, Windows XP, এবং Windows Server 2003-এর জন্য Windows Registry Editor Version 5.00।
- **ব্ল্যাঙ্ক লাইন**: একটি নতুন রেজিস্ট্রি পথের সূচনা চিহ্নিত করে।
- **RegistryPathx**: সাবকির পাথ যা আপনার আমদানি করা প্রথম মানটি ধারণ করে।
- **DataItemNamex**: আপনি যে ডেটা আইটেম আমদানি করতে চান তার নাম।
- **DataTypex**: রেজিস্ট্রি মানের জন্য ডেটা টাইপ।

নিম্নলিখিত সিনট্যাক্স ব্যবহার করে কীগুলি .reg ফাইলগুলিতে সংরক্ষণ করা হয়:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
আপনি মান নাম এর পরিবর্তে @ ব্যবহার করে একটি কী এর ডিফল্ট মান সম্পাদনা করতে পারেন:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### উদাহরণ

এখানে REG ফাইলের একটি উদাহরণ
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## তথ্যসূত্র

* [উইন্ডোজ রেজিস্ট্রি- উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Windows_Registry)

* [কীভাবে একটি .reg ফাইল ব্যবহার করে রেজিস্ট্রি সাবকি এবং মানগুলি যোগ, পরিবর্তন বা মুছবেন](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- একটি-রেগ-ফাইল-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23 ব্যবহার করে রেজিস্ট্রি-সাবকি-এবং-মানগুলি


