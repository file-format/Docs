{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MSIX - একটি MSIX ফাইল কি?",
  "description":"MSIX ফাইল এবং API সম্পর্কে জানুন যেগুলি MSIX ফাইল তৈরি করতে এবং খুলতে পারে৷",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## একটি MSIX ফাইল কি?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. এটি [APPX](/programming/appx/) এবং MSI-এর তুলনায় আধুনিক প্যাকেজ ফাইল ফর্ম্যাট যা শেষ পর্যন্ত এই নতুন ফাইল ফর্ম্যাটে পর্যায়ক্রমে আউট করা হবে৷ এটি Win32, WPF, এবং Windows Forms অ্যাপ স্থাপনের জন্য ব্যবহার করা যেতে পারে। MSIX ফাইলগুলি নির্ভরযোগ্য, এবং লক্ষ্য নেটওয়ার্ক এবং ডিস্ক স্পেস অপ্টিমাইজেশান। বিকাশকারীরা মাইক্রোসফ্ট স্টোর (আগে উইন্ডোজ স্টোর নামে পরিচিত) এর মাধ্যমে শেষ ব্যবহারকারীদের জন্য প্রোগ্রাম বিতরণ করতে এগুলি ব্যবহার করে।

## MSIX ফাইল ফরম্যাট - আরও তথ্য

MSIX ফাইলগুলি [ZIP](/compression/zip/)-সংকুচিত, সমস্ত ফাইল প্যাকেজ করা ফাইলের মধ্যে অন্তর্ভুক্ত। অ্যাপ সম্পর্কিত ফাইলগুলি ছাড়াও, MSIX ফাইলে [.xml](/web/xml/) কনফিগারেশন ফাইল রয়েছে যাতে অ্যাপ ইনস্টলেশন সম্পর্কিত তথ্য থাকে।

## একটি MSIX প্যাকেজের ভিতরে কী আছে?

একটি MSIX প্যাকেজ নিম্নলিখিত ফাইলগুলি নিয়ে গঠিত।

 * `AppxBlockMap.xml` - প্যাকেজ ব্লক ম্যাপ ফাইল হিসেবে পরিচিত, এটি একটি XML ডকুমেন্ট যাতে প্যাকেজে সংরক্ষিত ডেটার প্রতিটি ব্লকের জন্য ইনডেক্স এবং ক্রিপ্টোগ্রাফিক হ্যাশ সহ অ্যাপের ফাইলগুলির একটি তালিকা থাকে।
 * `AppxManifest.xml` - একটি XML নথি যাতে একটি MSIX অ্যাপ স্থাপন, প্রদর্শন এবং আপডেটের জন্য প্রয়োজনীয় তথ্য থাকে। এই তথ্যে প্যাকেজ পরিচয়, প্যাকেজ নির্ভরতা, প্রয়োজনীয় ক্ষমতা, ভিজ্যুয়াল উপাদান এবং এক্সটেনসিবিলিটি পয়েন্ট অন্তর্ভুক্ত রয়েছে।
 * `AppxSignature.p7x` - একটি ফাইল যা প্যাকেজ স্বাক্ষরিত হলে তৈরি হয়। সমস্ত MSIX প্যাকেজ ইনস্টল করার আগে স্বাক্ষর করতে হবে। AppxBlockmap.xml এর সাথে, প্ল্যাটফর্মটি প্যাকেজটি ইনস্টল করতে এবং যাচাই করতে সক্ষম।

## তথ্যসূত্র

 * [MSIX ওভারভিউ](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Microsoft Visual Studio ব্যবহার করে APPX ফাইল তৈরি করুন](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

