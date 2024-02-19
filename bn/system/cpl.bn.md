{
  "date": "2021-06-29",
  "keywords": [
    "CPL",
    "extension",
    "file",
    "format",
    "system",
    "Control Panel File",
    "Windows",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "CPL - কন্ট্রোল প্যানেল ফাইল",
  "description": "CPL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CPL ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cpl-bn"
    }
  },
  "lastmod": "2021-06-29"
}

## একটি CPL ফাইল কি? ##

একটি CPL ফাইল হল এক ধরনের সিস্টেম ফাইল। এটি উইন্ডোজ অপারেটিং সিস্টেম দ্বারা ব্যবহৃত হয়। একটি CPL ফাইল কন্ট্রোল প্যানেল ফাইলের জন্য ছোট। এই ফাইলগুলি হল বাইনারি ফাইল যা মাইক্রোসফ্ট উইন্ডোজ অপারেটিং সিস্টেমে কন্ট্রোল প্যানেলের সাথে খোলে এবং নিয়ন্ত্রণ প্যানেলে উপলব্ধ সরঞ্জামগুলিকে উপস্থাপন করতে এবং খুলতে ব্যবহৃত হয়, যেমন মাউস, ডিসপ্লে, নেটওয়ার্কিং, অন্যদের মধ্যে। CPL ফাইলগুলি সাধারণত আপনার ডিভাইসের সিস্টেম ফোল্ডারে সংরক্ষণ করা হয়। এই ফাইলগুলি ম্যানুয়ালি খোলা উচিত নয়।


## CPL ফাইল ফরম্যাট ##

আপনার উইন্ডোজ অপারেটিং সিস্টেমের বিভিন্ন CPL ফাইল বিভিন্ন কন্ট্রোল প্যানেল আইটেম প্রতিনিধিত্ব করার জন্য সংযুক্ত করা হয়। সমস্ত কন্ট্রোল প্যানেল আইটেম একটি CPL ফাইলের সাথে লিঙ্ক করা হয় এবং তাদের আইটেমগুলির সাথে .cpl প্রত্যয় সংযুক্ত থাকে।

কিছু সাধারণ ধরনের CPL ফাইলের বিন্যাস হল:

* Inetcpl.cpl - আপনার ডিভাইসে ইন্টারনেট বৈশিষ্ট্যের জন্য

* Appwiz.cpl - আপনার ডিভাইসে প্রোগ্রাম বৈশিষ্ট্য যোগ বা সরাতে

* Desk.cpl - প্রদর্শন বৈশিষ্ট্যের জন্য

* Main.cpl - মাউস, ফন্ট, কীবোর্ড এবং প্রিন্টার সম্পর্কিত বৈশিষ্ট্যগুলির জন্য। 

* Netcpl.cpl - নেটওয়ার্ক সম্পর্কিত বৈশিষ্ট্যগুলির জন্য

* System.cpl - সিস্টেম সম্পর্কিত বৈশিষ্ট্য এবং নতুন হার্ডওয়্যার উইজার্ড যোগ করার জন্য

* TimeDate.cpl - তারিখ বা সময় বৈশিষ্ট্যের জন্য

* Mlcfg32.cpl - মাইক্রোসফ্ট এক্সচেঞ্জ বা উইন্ডোজ মেসেজিং বৈশিষ্ট্যের জন্য

* Intl.cpl - এটি আঞ্চলিক সেটিংস বৈশিষ্ট্যের সাথে সম্পর্কিত

* Modem.cpl - মডেম সম্পর্কিত বৈশিষ্ট্যের জন্য

* Themes.cpl - ডেস্কটপ থিম এবং বৈশিষ্ট্য সংরক্ষণ করে। 

* Password.cpl - পাসওয়ার্ড বৈশিষ্ট্যের জন্য

* Mmsys.cpl - মাল্টিমিডিয়া বৈশিষ্ট্যের জন্য

* Wgpocpl.cpl - মাইক্রোসফ্ট মেল পোস্ট অফিসের সাথে সম্পর্কিত


## সংক্ষিপ্ত ইতিহাস ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. এটি এখনও সমস্ত উইন্ডোজ সংস্করণে ব্যবহৃত হয়, এবং সমস্ত কন্ট্রোল প্যানেল আইটেম বৈশিষ্ট্য এই ফাইল প্রকার ব্যবহার করে সংরক্ষণ করা হয়।

## CPL উদাহরণ ##

একটি নমুনা CPL ফাইল নীচে দেখা যেতে পারে:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
