{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XFDF ফাইল ফরম্যাট - একটি XFDF ফাইল কি?",
  "description":"XFDF ফাইল এবং API সম্পর্কে জানুন যেগুলি XFDF ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## একটি XFDF ফাইল কি?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF ফাইল ফরম্যাট - আরও তথ্য

XFDF ফাইলগুলি XML ফাইল ফর্ম্যাটে সংরক্ষিত হয় যা ডেটা আমদানি এবং রপ্তানির জন্য ব্যবহৃত একটি সর্বজনীন বিন্যাস। একটি XFDF ফাইল কাঠামো একটি শিরোনাম নিয়ে গঠিত, তারপরে ফিল্ডের মান এবং উপাদান ডেটা নীচে দেখানো হয়েছে।

|এলিমেন্ট|অ্যাট্রিবিউট|কন্টেন্ট|
---|---|---|
|\<XFDF> ||সর্বোচ্চ উপাদান|
|\<fields> ||এই টেমপ্লেটের জন্য সমস্ত ক্ষেত্রের মান|
|<field (T)> |নাম |ক্ষেত্রের নাম |
|<value (V)> |মান |ক্ষেত্রের মান |

## তথ্যসূত্র

* [অ্যাক্রোব্যাট দ্বারা এফডিএফ ফর্ম্যাট সমর্থন](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)
