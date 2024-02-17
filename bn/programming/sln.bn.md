{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SLN",
  "description":"Learn about এসএলএন file format and APIs that can create and open এসএলএন files.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## এসএলএন ফাইল কি?
.এসএলএন এক্সটেনশন সহ একটি ফাইল একটি **ভিজ্যুয়াল স্টুডিও সমাধান** ফাইল উপস্থাপন করে যা একটি সমাধান ফাইলে প্রকল্পগুলির সংগঠন সম্পর্কে তথ্য রাখে। এই ধরনের সমাধান ফাইলের বিষয়বস্তু ফাইলের ভিতরে প্লেইন টেক্সটে লেখা থাকে এবং যেকোন টেক্সট এডিটরে ফাইলটি খোলার মাধ্যমে পর্যবেক্ষণ/সম্পাদনা করা যায়। একটি সমাধান ফাইলে থাকা তথ্য স্থায়ী থাকে এবং সমাধানের সাথে সম্পর্কিত তথ্য যেমন [projects ](/programming/csproj/) এবং অন্যান্য প্রয়োজনীয় তথ্য লোড করতে ব্যবহৃত হয়। সমাধান ফাইল দ্বারা উল্লেখ করা প্রকল্প ফাইলগুলিতে সেই প্রকল্পের আইটেমগুলির সাথে শ্রেণিবিন্যাসের জন্য পরিবেশ সক্ষম করার জন্য অতিরিক্ত তথ্য রয়েছে। .sln ফাইলে কোনো তথ্য সংরক্ষণ করা হয় না, যদিও প্রয়োজনে প্রকল্পের তথ্য .sln ফাইলে লেখা যেতে পারে।

## **এসএলএন সংস্করণ ইতিহাস** ##

সমাধান ফরম্যাট সংস্করণটি সময়ের সাথে সাথে প্রতিটি মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও সমাধানের সাথে বিকশিত হয়েছে। এ সম্পর্কে বিস্তারিত নিম্নরূপ।


|ভিজ্যুয়াল স্টুডিও সংস্করণ|সমাধান বিন্যাস সংস্করণ
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **একটি সমাধান ফাইলের বিষয়বস্তু** ###

একটি সমাধান ফাইল প্রকল্প লোড করার জন্য পরিবেশ দ্বারা পড়া হয় যে বিভিন্ন বিভাগ গঠিত. একটি নমুনা .sln ফাইলের বিষয়বস্তু নীচে দেখানো হয়েছে।

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **প্রকল্প ঘোষণা** ###

একটি সলিউশন ফাইলে একাধিক প্রজেক্ট ডিক্লেয়ারেশন থাকতে পারে এবং তাও ভিন্ন ধরনের প্রোজেক্টের। উদাহরণস্বরূপ, একটি একক সমাধান ফাইলে একটি CSharp পাশাপাশি একটি VB.NET প্রকল্প থাকতে পারে। এই প্রকারগুলিকে [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) ব্যবহার করে একটি সমাধানে আলাদা করা হয়৷ স্পষ্ট বোঝার জন্য উপরোক্ত প্রকল্প ঘোষণাকে অনুসরণ হিসাবে সাধারণীকরণ করা যেতে পারে।

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`প্রজেক্ট-টাইপ-জিইউআইডি:` প্রজেক্ট-টাইপ-জিইউআইডি বিভিন্ন ধরনের প্রকল্পের জন্য অনন্য এবং সমাধান পাঠক প্রকল্পের ধরন শনাক্ত করতে ব্যবহার করে। এই ক্ষেত্রে, F184B08F-C81C-45F6-A57F-5ABD9991F28F দেখায় যে এটি একটি VB.NET প্রকল্প।

`প্রকল্প GUID:` প্রকল্পের অনন্য GUID যা সমাধানের অন্যান্য প্রকল্প থেকে এটিকে আলাদা করে। সমাধানে একটি প্রকল্পের অনন্য আইডি সমাধানের অন্যান্য প্রকল্পগুলির জন্য এটি অ্যাক্সেস করা সম্ভব করে তোলে।

.sln ফাইলের প্রকল্প বিভাগে থাকা তথ্যের উপর ভিত্তি করে, পরিবেশ প্রতিটি প্রকল্প ফাইল লোড করে। তারপরে প্রকল্পটি নিজেই প্রকল্পের শ্রেণিবিন্যাসের জন্য দায়ী এবং কোনও নেস্টেড প্রকল্প লোড করার জন্য দায়ী। সমাধানে করা যেকোনো পরিবর্তন প্রকল্পটি সংরক্ষণ বা বন্ধ করার পরে সমাধান ফাইলে ফিরে সংরক্ষিত হয়।

## ভিজ্যুয়াল স্টুডিও সমাধান VS প্রকল্প

**প্রকল্প:** যৌক্তিকভাবে, আপনি যখন ভিজ্যুয়াল স্টুডিও ব্যবহার করে একটি অ্যাপ বা সফ্টওয়্যার তৈরি করতে শুরু করেন, আপনি একটি নতুন প্রকল্প শুরু করেন। একটি প্রজেক্টে সোর্স কোড, আইকন, ছবি, ডেটা ফাইল এবং আরও অনেক কিছুর মতো প্রয়োজনীয় ফাইল থাকে যা একটি এক্সিকিউটেবল অ্যাপ, ওয়েবসাইট বা লাইব্রেরিতে কম্পাইল করা হবে।

**সমাধান:** একটি সমাধানে এক বা একাধিক প্রকল্প থাকে। সুতরাং সমাধানটি ভিজ্যুয়াল স্টুডিও প্রকল্পগুলির জন্য একটি পাত্রের মতো। যৌক্তিকভাবে, আমরা বলতে পারি যে কেউ তার ব্যবসার জন্য একটি ওয়েবসাইট, ডেস্কটপ অ্যাপ, শান্ত পরিষেবা এবং মোবাইল অ্যাপ সহ একটি সম্পূর্ণ সমাধান পেতে চায়।

### **রেফারেন্স** ###

* [সমাধান ফাইল - MSDN দ্বারা](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [প্রজেক্ট টাইপ GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


