{
  "date": "2019-10-11",
  "keywords": [
    "csproj file",
    "csproj",
    "extension",
    "format",
    "What is a csproj file",
    "csproj file format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "CSPROJ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CSPROJ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-csproj-bn"
    }
  },
  "lastmod": "2021-05-21"
}

## একটি CSProj ফাইল কি?
CSPROJ এক্সটেনশন সহ ফাইলগুলি একটি C# প্রজেক্ট ফাইল উপস্থাপন করে যাতে সিস্টেম অ্যাসেম্বলির রেফারেন্স সহ একটি প্রকল্পে অন্তর্ভুক্ত ফাইলগুলির তালিকা থাকে। যখন মাইক্রোসফট VIiual স্টুডিওতে একটি নতুন প্রজেক্ট শুরু করা হয়, তখন আপনি মূল সমাধান ([.sln](/programming/sln/)) ফাইল সহ একটি .csproj ফাইল পাবেন। যদি একটি প্রজেক্টে একাধিক অ্যাসেম্বলি থাকে, তাহলে সেখানে সমান সংখ্যক প্রোজেক্ট ফাইল থাকবে যেখানে .sln ফাইল প্রোজেক্টের অংশ হিসাবে সেগুলিকে একত্রিত করে। এই ফাইলের বিষয়বস্তুগুলি প্রকল্পটি তৈরি করতে প্রয়োজনীয় সমস্ত প্রয়োজনীয়তা যেমন অন্তর্ভুক্ত করার জন্য সামগ্রী, প্ল্যাটফর্মের প্রয়োজনীয়তা, সংস্করণের তথ্য, ওয়েব সার্ভার বা ডাটাবেস সার্ভার সেটিংস এবং যে কাজগুলি সম্পাদন করতে হবে তা সংজ্ঞায়িত করে৷ একটি প্রজেক্ট ফাইলের বিষয়বস্তু XML ফাইল ফরম্যাটে সাজানো হয় এবং সম্পাদনার পাশাপাশি দেখার জন্য যেকোনো টেক্সট এডিটরে খোলা যেতে পারে। এটি যথাযথ ব্যবস্থার জন্য প্রকল্প ফাইলগুলির একটি যৌক্তিক দৃশ্যও দেয়।

## CSPROJ ফাইল ফরম্যাট #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

নিম্নলিখিত বিভাগগুলি একটি প্রকল্প ফাইলের জন্য ফাইল বিন্যাসের উপাদানগুলিকে বিশদভাবে বর্ণনা করে৷

### প্রকল্পের উপাদান ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) উপাদানটি প্রতিটি প্রকল্প ফাইলের মূল উপাদান। এটি প্রোজেক্ট ফাইলের জন্য XML স্কিমা সনাক্ত করে এবং বিল্ড প্রক্রিয়ার জন্য এন্ট্রি পয়েন্টগুলি নির্দিষ্ট করার জন্য বৈশিষ্ট্যগুলি অন্তর্ভুক্ত করতে পারে।

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### বৈশিষ্ট্য এবং শর্তাবলী

বৈশিষ্ট্যগুলি একটি প্রকল্প তৈরি করার জন্য প্রয়োজনীয় প্রয়োজনীয় তথ্য উপস্থাপন করে। এই ধরনের বৈশিষ্ট্য একটি [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) উপাদানের মধ্যে সংজ্ঞায়িত করা হয়। এই বৈশিষ্ট্যগুলি কী-মান জোড়া নিয়ে গঠিত যেখানে সম্পত্তি উপাদানের নাম প্রপার্টি কীকে সংজ্ঞায়িত করে এবং উপাদানটির বিষয়বস্তু সম্পত্তির মান নির্ধারণ করে। উদাহরণস্বরূপ, আপনি একটি স্ট্যাটিক সার্ভারের নাম এবং সংযোগ স্ট্রিং সংরক্ষণ করতে ServerName এবং ConnectionString নামের বৈশিষ্ট্যগুলি সংজ্ঞায়িত করতে পারেন।

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

উপাদানের মূল্যায়নের মানদণ্ড নির্দিষ্ট করার জন্য উপাদানগুলির মাধ্যমে শর্তগুলি নির্দিষ্ট করা যেতে পারে। নীচে দেখানো হিসাবে সম্পত্তি সংজ্ঞায়িত করার সময় এটি শর্ত শব্দ দ্বারা নির্দিষ্ট করা হয়:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

যখন MSBuild এই সম্পত্তির সংজ্ঞা প্রক্রিয়া করে, এটি প্রথমে একটি **$(OutputRoot)** সম্পত্তির মান উপলব্ধ কিনা তা পরীক্ষা করে। যদি সম্পত্তির মান ফাঁকা থাকে—অন্য কথায়, ব্যবহারকারী এই সম্পত্তির জন্য কোনো মান প্রদান করেননি—শর্তটি **সত্য**-এ মূল্যায়ন করা হয় এবং সম্পত্তির মান **..\Publish\Out.** এ সেট করা হয়।

### আইটেম এবং আইটেম গ্রুপ

একটি প্রকল্প ফাইল বিল্ড প্রক্রিয়ার ইনপুটগুলিকে সংজ্ঞায়িত করে যা আসলে বিভিন্ন ধরনের ফাইল। MSBuild নামকরণে, এই ইনপুটগুলি আইটেম উপাদান দ্বারা প্রতিনিধিত্ব করা হয় এবং একটি [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) উপাদানের মধ্যে সংজ্ঞায়িত করা হয়। ঠিক **সম্পত্তি** উপাদানগুলির মতো, আপনি একটি **আইটেম** উপাদানের নাম দিতে পারেন যা আপনি চান৷ যাইহোক, আইটেমটি যে ফাইল বা ওয়াইল্ডকার্ডটি উপস্থাপন করে তা সনাক্ত করতে আপনাকে অবশ্যই একটি **অন্তর্ভুক্ত** বৈশিষ্ট্য উল্লেখ করতে হবে।

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### লক্ষ্য এবং কাজ

একটি [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) উপাদান একটি পৃথক বিল্ড নির্দেশনা (বা কাজ) উপস্থাপন করে। MSBuild পূর্বনির্ধারিত অনেকগুলি কাজ অন্তর্ভুক্ত করে। উদাহরণ স্বরূপ:

* **কপি** টাস্ক ফাইলগুলিকে একটি নতুন স্থানে কপি করে।

* **Csc** কাজটি ভিজ্যুয়াল C# কম্পাইলারকে আহ্বান করে।

* **Vbc** টাস্কটি ভিজ্যুয়াল বেসিক কম্পাইলারকে আহ্বান করে।

* **Exec** টাস্ক একটি নির্দিষ্ট প্রোগ্রাম চালায়।

* **মেসেজ** টাস্ক একজন লগারকে একটি বার্তা লেখে।


কার্যগুলি সর্বদা [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) উপাদানগুলির মধ্যে থাকতে হবে৷ একটি **টার্গেট** এলিমেন্ট হল এক বা একাধিক টাস্কের একটি সেট যা ক্রমানুসারে সম্পাদিত হয় এবং একটি প্রোজেক্ট ফাইলে একাধিক টার্গেট থাকতে পারে।

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## তথ্যসূত্র

* [প্রজেক্ট ফাইল বোঝা - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- ফাইল)


