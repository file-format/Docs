{
  "date": "2019-12-03",
  "keywords": [
    "DOCX",
    "file",
    "format",
    "file type",
    "extension",
    "what is an DOCX file?"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "DOCX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা DOCX ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-docx-bn"
    }
  },
  "lastmod": "2019-12-03"
}

## একটি DOCX ফাইল কি? ##

DOCX Microsoft Word নথিগুলির জন্য একটি সুপরিচিত বিন্যাস। মাইক্রোসফ্ট অফিস 2007 প্রকাশের সাথে 2007 থেকে প্রবর্তিত, এই নতুন নথি বিন্যাসের কাঠামোটি প্লেইন বাইনারি থেকে XML এবং বাইনারি ফাইলের সংমিশ্রণে পরিবর্তিত হয়েছিল। Docx ফাইলগুলি Word 2007 এবং পার্শ্বীয় সংস্করণগুলির সাথে খোলা যেতে পারে তবে MS Word এর আগের সংস্করণগুলির সাথে নয় যা DOC ফাইল এক্সটেনশন সমর্থন করে৷

## সংক্ষিপ্ত ইতিহাস ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX ফাইল ফরম্যাট স্পেসিফিকেশন - আরও তথ্য

একটি Docx ফাইল একটি জিপ সংরক্ষণাগার মধ্যে থাকা XML ফাইলগুলির একটি সংগ্রহ নিয়ে গঠিত। একটি নতুন ওয়ার্ড নথির বিষয়বস্তু আনজিপ করে দেখা যাবে। সংগ্রহে XML ফাইলগুলির একটি তালিকা রয়েছে যা এই শ্রেণীবদ্ধ করা হয়েছে:

* মেটাডেটা ফাইল - আর্কাইভে উপলব্ধ অন্যান্য ফাইল সম্পর্কে তথ্য রয়েছে

* নথি - নথির প্রকৃত বিষয়বস্তু রয়েছে৷


### মেটাডেটা ফাইল ###

মাইক্রোসফ্ট ওয়ার্ড ফাইলগুলির মধ্যে সম্পর্ক খুঁজে পেতে এবং নথির বিষয়বস্তুগুলি সনাক্ত করতে এই ফাইলগুলি ব্যবহার করে। যখন একটি Word নথি সংরক্ষণাগার নিষ্কাশন করা হয়, এটি নিচে বিস্তারিত হিসাবে এই ধরনের ফাইলের একটি সংখ্যা রয়েছে.

#### সম্পর্ক - \_rels/.rels ####

এই ফাইলটিতে এমন তথ্য রয়েছে যা MS Wordকে নথির বিষয়বস্তু এবং অন্যান্য রেফারেন্স কোথায় দেখতে হবে তা বলে। প্রতিটি সম্পর্ক একটি অনন্য সম্পর্ক আইডি দ্বারা চিহ্নিত করা হয় এবং উল্লেখিত XML ফাইলটিকে লক্ষ্য হিসাবে নির্দিষ্ট করে৷ একটি নমুনা সম্পর্ক ফাইল নিম্নলিখিত হিসাবে দেখানো হয়েছে:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### বিষয়বস্তুর প্রকার ####

একটি নথিতে ছবি, থিম, ওয়ার্ড আর্ট ইত্যাদির মতো বিভিন্ন মিডিয়া প্রকার থাকতে পারে৷ এই ধরনের একটি XML ফাইলের বিষয়বস্তু নিম্নরূপ দেখানো হয়েছে:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### সম্পদের উল্লেখ - \_rels/document.xml.rels ####

সম্পদ সম্পর্কে তথ্য, যেমন নথিতে এমবেড করা ছবি, এই XML ফাইলে উল্লেখ করা হয়েছে।

#### প্রধান নথির বিষয়বস্তু ####

এটি আর্কাইভের প্রধান XML ফাইলকে নির্দেশ করে যাতে ডকুমেন্টের পাঠ্য বিষয়বস্তু থাকে। এই বিষয়বস্তুটি OpenOffice XML স্পেসিফিকেশন অনুযায়ী বিভিন্ন নোড দ্বারা উপস্থাপিত হয়। বেশিরভাগই এই ফাইলের বিষয়বস্তু অনুচ্ছেদ এবং টেবিল নিয়ে গঠিত, যদিও সেগুলি অন্যান্য নোডও হতে পারে।

### ফাইল ফরম্যাট নোড ###

প্রধান document.xml ফাইল হল একটি ফাইলের সামগ্রিক বিষয়বস্তু উপস্থাপনের জন্য নোডের একটি সংগ্রহ। প্রতিটি নোডের একটি শুরু এবং শেষ থাকে যা হয় আরও নোড বা বিষয়বস্তুকে অন্তর্ভুক্ত করে। এই ধরনের একটি xml ফাইলের একটি সরলীকৃত উদাহরণ নিম্নরূপ:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

বিষয়বস্তু উপস্থাপনের জন্য একটি DOCX ফাইলে থাকা কিছু নোডের তথ্য নিচে দেওয়া হল।

`<w:document> ` - ফাইলের মূল বিষয়বস্তুর মূল উপাদানের প্রতিনিধিত্ব করে।

`<w:body> ` - নথির মূল অংশকে প্রতিনিধিত্ব করে যা অন্যান্য অনেক উপাদান নোড যেমন অনুচ্ছেদ, টেবিল এবং বিভাগগুলি নিয়ে গঠিত হতে পারে।

#### অনুচ্ছেদ ####

একটি অনুচ্ছেদ একটি নথির মধ্যে প্রধান বিষয়বস্তু ধারক. এটি ** দ্বারা প্রতিনিধিত্ব করা হয়<w:p> ** একটি নথির মধ্যে উপাদান। একটি অনুচ্ছেদ আরও এক বা একাধিক রান নিয়ে গঠিত **<w:r> ** যেটিতে অনুচ্ছেদের প্রকৃত পাঠ্য রয়েছে। রান ছাড়াও, অনুচ্ছেদে অন্যান্য নথি উপাদান যেমন হাইপারলিঙ্ক, মন্তব্য ইত্যাদি থাকতে পারে। একটি উদাহরণ অনুচ্ছেদ গঠন নীচে দেখানো হয়েছে:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## DOCX FAQs

 * **DOCX কি একটি ফাইল এক্সটেনশন?** - মাইক্রোসফ্ট ওয়ার্ড 2007 এবং পরবর্তী ফাইল ফরম্যাটগুলিকে Word ফাইলগুলি সঞ্চয় করার জন্য ব্যবহার করার জন্য DOCX ফাইল এক্সটেনশন হিসাবে ব্যবহৃত হয়। এটি আপনার ওএসকেও বলে যে এই DOCX ফাইলটি খুলতে এবং এর আইকনটি দেখানোর জন্য Microsoft Word 2007 প্রয়োজন৷
 * **DOCX কি Word এর মতই** - DOCX হল একটি ফাইল ফরম্যাট যা Microsoft Word দ্বারা ওপেন XML ফরম্যাটে নথি সংরক্ষণ করতে ব্যবহৃত হয়। ওয়ার্ড, অন্যদিকে, মাইক্রোসফ্ট অফিসের একটি অ্যাপ্লিকেশন সফ্টওয়্যার যা অন্যান্য ফাইল ফর্ম্যাট যেমন DOC, DOT, DOTM এবং অন্যান্যগুলিকে সমর্থন করে।
 * **DOC এবং DOCX পার্থক্য কি** - DOC হল Word 2007 এবং আগের ফাইল ফরম্যাটে সংরক্ষিত ওয়ার্ড ফাইল। DOCX Microsoft 2007 এবং পরবর্তী সংস্করণ দ্বারা সমর্থিত Open XML ফাইল ফরম্যাটের উপর ভিত্তি করে। আরও বিশদ বিবরণের জন্য [DOC এবং DOCX-এর মধ্যে পার্থক্য](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) দেখুন।

## তথ্যসূত্র ##

* [MS - DOCX ফাইল ফরম্যাট](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [অফিস ওপেন এক্সএমএল](http://officeopenxml.com/)


