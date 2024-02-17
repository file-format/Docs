{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADM ফাইল - প্রশাসনিক টেমপ্লেট ফাইল বিন্যাস",
  "description":"ADM ফাইল ফরম্যাট এবং কিভাবে ADM ফাইল খুলতে হয় সে সম্পর্কে জানুন।",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm-bn",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## একটি ADM ফাইল কি?

একটি ADM ফাইল হল একটি টেমপ্লেট ফাইল যা Microsoft Group Policies সফ্টওয়্যার দ্বারা রেজিস্ট্রি ফাইলে রেজিস্ট্রি-ভিত্তিক নীতি সেটিংসের অবস্থান নির্দিষ্ট করতে ব্যবহৃত হয়। এটি সিস্টেম অ্যাডমিনিস্ট্রেটরদের দ্বারা গ্রুপের অংশ কম্পিউটারগুলির একটি গ্রুপ পরিচালনার জন্য নীতি নির্ধারণ করতে ব্যবহৃত হয়। এই তথ্য গ্রুপ পলিসি অবজেক্টের (GPOs) অংশ হয়ে যায় যা গ্রুপ পরিচালনার জন্য তৈরি করা হয়।

আপনি Microsoft গ্রুপ পলিসি অবজেক্ট এডিটর ব্যবহার করে ADM ফাইল খুলতে পারেন।

## এডিএম ফাইল ফরম্যাট - আরও তথ্য

ADM ফাইলগুলি ইউনিকোড-ফরম্যাটেড টেক্সট ফাইল হিসাবে সংরক্ষণ করা হয়। এগুলি প্রাথমিকভাবে Windows Vista এবং Windows 7 রেজিস্ট্রিতে রেজিস্ট্রি-ভিত্তিক নীতি সেটিংসের অবস্থান বর্ণনা করতে ব্যবহৃত হত।

ADM ফাইলগুলি আর সমর্থিত নয় এবং [ADMX](/system/admx/) ফাইলগুলি দ্বারা প্রতিস্থাপিত হয়েছে৷ মাইক্রোসফ্ট উইন্ডোজ ভিস্তা সার্ভিস প্যাক 1 বা তার পরে চলমান কম্পিউটারগুলিতে GPA নিম্নলিখিত ডিফল্ট ADM ফাইলগুলিকে উপেক্ষা করে৷

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## তথ্যসূত্র

* [প্রশাসনিক টেমপ্লেট ফাইল - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ - প্রশাসনিক টেমপ্লেট ফাইল পরিচালনা করা](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


