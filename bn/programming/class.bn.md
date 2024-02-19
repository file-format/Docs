{
  "date": "2019-10-11",
  "keywords": [
    "class",
    ".class",
    "what is a class file",
    "how to open a class file",
    "extension",
    "file",
    "class file",
    "class file format",
    ".class extension",
    "class file in java"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ক্লাস - জাভা ক্লাস ফাইল ফরম্যাট",
  "description": "ক্লাস ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা ক্লাস ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-class-bn"
    }
  },
  "lastmod": "2020-09-10"
}

## ক্লাস ফাইল কি?

জাভাতে একটি **ক্লাস ফাইল** হল [.java](/programming/java/) ক্লাসের কম্পাইল করা আউটপুট যা আসলে একটি জাভা ভার্চুয়াল মেশিন (JVM) দ্বারা কার্যকর করা হয়। ক্লাস ফাইলগুলি পৃথকভাবে চালানো যেতে পারে পাশাপাশি অন্যান্য প্যাকেজ ফাইলগুলির সাথে একটি বান্ডেল হিসাবে একটি [JAR](/programming/jar/) ফাইলের একটি অংশ হতে পারে৷ এগুলি কমান্ড লাইন ইন্টারফেস থেকে **`javac`** কমান্ড ব্যবহার করে তৈরি করা যেতে পারে। কিছু জাভা আইডিই যেমন [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) এবং NetBeans প্রোজেক্টের জাভা ফাইল থেকে .class আউটপুট ফাইল তৈরি করে।

## ক্লাস ফাইল ফরম্যাট

একটি জাভা ক্লাস ফাইল বাইটকোড নিয়ে গঠিত যা JVM দ্বারা চালানোর জন্য মধ্যবর্তী কোড। একটি ক্লাস ফাইলে 8-বিট বাইটের একটি স্ট্রীম থাকে এবং মাল্টিবাইট ডেটা আইটেম সবসময় বড়-এন্ডিয়ান ক্রমে সংরক্ষণ করা হয়।

### ক্লাসফাইল স্ট্রাকচার

ক্লাস ফাইল স্ট্রাকচার নিচে দেখানো হয়েছে।
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
কোথায়:

* u1 = স্বাক্ষরবিহীন এক-বাইটের পরিমাণ

* u2 = স্বাক্ষরবিহীন দুই-বাইটের পরিমাণ

* u4 = স্বাক্ষরবিহীন চার-বাইটের পরিমাণ


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `ম্যাজিক` - ম্যাজিক আইটেমটি ক্লাস ফাইল ফরম্যাট চিহ্নিত করে ম্যাজিক নম্বর সরবরাহ করে; এর মান 0xCAFEBABE আছে।

* `minor_version`, `major_version` - minor_version এবং major_version আইটেমগুলির মান হল এই ক্লাস ফাইলের ছোট এবং বড় সংস্করণ সংখ্যা।

* `ধ্রুবক_পুল_গণনা` - ধ্রুবক_পুল_গণনা আইটেমের মান ধ্রুবক_পুল টেবিল প্লাস ওয়ানের এন্ট্রির সংখ্যার সমান। একটি ধ্রুবক_পুল সূচক বৈধ বলে বিবেচিত হয় যদি এটি শূন্যের চেয়ে বড় এবং ধ্রুবক_পুল_গণনার চেয়ে কম হয়, দীর্ঘ এবং দ্বিগুণ ধরণের ধ্রুবকের জন্য ব্যতিক্রম।

* `ধ্রুবক_পুল[]` - ধ্রুবক_পুল হল কাঠামোর একটি সারণী (§4.4) যা বিভিন্ন স্ট্রিং ধ্রুবক, শ্রেণী এবং ইন্টারফেসের নাম, ক্ষেত্রের নাম এবং অন্যান্য ধ্রুবককে প্রতিনিধিত্ব করে যা ClassFile কাঠামো এবং এর সাবস্ট্রাকচারের মধ্যে উল্লেখ করা হয়। প্রতিটি constant_pool টেবিল এন্ট্রির বিন্যাস তার প্রথম "ট্যাগ" বাইট দ্বারা নির্দেশিত হয়।

* `অ্যাক্সেস_ফ্ল্যাগস` - অ্যাক্সেস_ফ্ল্যাগ আইটেমের মান হল পতাকাগুলির একটি মাস্ক যা এই ক্লাস বা ইন্টারফেসের অ্যাক্সেস অনুমতি এবং বৈশিষ্ট্যগুলি বোঝাতে ব্যবহৃত হয়।

* `this_class` - এই_শ্রেণির আইটেমের মান অবশ্যই ধ্রুবক_পুল টেবিলে একটি বৈধ সূচক হতে হবে।

* `সুপার_ক্লাস` - একটি ক্লাসের জন্য, সুপার_ক্লাস আইটেমের মান অবশ্যই শূন্য হতে হবে অথবা ধ্রুবক_পুল টেবিলে একটি বৈধ সূচক হতে হবে।

* `ইন্টারফেস_গণনা` - ইন্টারফেস_কাউন্ট আইটেমের মান এই শ্রেণী বা ইন্টারফেস প্রকারের সরাসরি সুপার ইন্টারফেসের সংখ্যা দেয়।

* `ইন্টারফেস[]` - ইন্টারফেস অ্যারের প্রতিটি মান অবশ্যই ধ্রুবক_পুল টেবিলের একটি বৈধ সূচক হতে হবে।

* `ক্ষেত্র_গণনা` - ক্ষেত্র_গণনা আইটেমের মান ফিল্ড টেবিলে ক্ষেত্র_তথ্য কাঠামোর সংখ্যা দেয়।

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `পদ্ধতি_গণনা` - পদ্ধতি_গণনা আইটেমের মান পদ্ধতি টেবিলে পদ্ধতি_তথ্য কাঠামোর সংখ্যা দেয়।

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` - গুণাবলী_গণনা আইটেমের মান এই শ্রেণীর বৈশিষ্ট্য সারণীতে বৈশিষ্ট্যের সংখ্যা (§4.7) দেয়।

* `অ্যাট্রিবিউটস[]` - অ্যাট্রিবিউট টেবিলের প্রতিটি মান অবশ্যই একটি অ্যাট্রিবিউট_ইনফো স্ট্রাকচার হতে হবে।





## তথ্যসূত্র

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

