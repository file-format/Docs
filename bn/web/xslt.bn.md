{
  "date": "2021-01-20",
  "keywords": [
    "xslt",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "Extensible Stylesheet Language"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XSLT ফাইল ফরম্যাট",
  "description": "XSLT ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা XSLT ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xslt-bn"
    }
  },
  "lastmod": "2021-01-20"
}

## একটি XSLT ফাইল কি?

একটি .xslt এক্সটেনশন সহ একটি ফাইল হল একটি এক্সটেনসিবল স্টাইলশীট ল্যাঙ্গুয়েজ ট্রান্সফরমেশন ফাইল যা XSL নির্দেশাবলী ব্যবহার করে একটি XML ফাইলকে রূপান্তর ও স্টাইল করতে ব্যবহৃত হয়। ফরম্যাটটি XML ডকুমেন্টকে টেক্সট ডকুমেন্ট বা .html ওয়েব পেজের মতো স্ট্যান্ডার্ড আউটপুট ফরম্যাটে রূপান্তর করতে ব্যবহৃত হয়। এই রূপান্তরটি বিদ্যমান XML নথির বিষয়বস্তুর উপর ভিত্তি করে একটি নতুন নথি তৈরি করে। XSLT এটিকে তাত্ত্বিকভাবে নির্বিচারে গণনা করতে সক্ষম করে তুলছে।

## XSLT ফাইল ফরম্যাট

XLST ফাইল ফরম্যাটে প্লেইন টেক্সট ফরম্যাটে রূপান্তর নির্দেশাবলী রয়েছে যা যেকোনো টেক্সট এডিটরে দেখা যেতে পারে। ভাষার তিনটি সংশোধন করা হয়েছে।

* `XSLT 1.0` - XSLT 1.0 একটি W3C সুপারিশ হিসাবে 1999 সালের নভেম্বরে প্রকাশিত হয়েছিল।

* `XSLT 2.0` - এটিতে তারিখ, সময় এবং সময়কাল ম্যানিপুলেট করার জন্য নিয়মিত এক্সপ্রেশন, ফাংশন এবং অপারেটর ব্যবহার করে স্ট্রিং ম্যানিপুলেশন, একাধিক আউটপুট নথি, গ্রুপিং, এবং একটি সমৃদ্ধ টাইপ সিস্টেম এবং শক্তিশালী টাইপ চেকিংয়ের মতো পরিবর্তনগুলি অন্তর্ভুক্ত রয়েছে।

* `XSLT 3.0` - এটি 8 জুন 2017-এ W3C সুপারিশের অংশ হয়ে ওঠে এবং প্রধান নতুন বৈশিষ্ট্যগুলির মধ্যে রয়েছে স্ট্রিমিং রূপান্তর, বড় স্টাইলশিটের মডুলারিটি উন্নত করার জন্য প্যাকেজ, ডায়নামিক ত্রুটিগুলির উন্নত পরিচালনা, উদাহরণস্বরূপ, একটি xsl: চেষ্টা করার নির্দেশ, এবং মানচিত্র এবং অ্যারেগুলির জন্য সমর্থন, XSLT কে JSON এর পাশাপাশি XML পরিচালনা করতে সক্ষম করে।


### XSLT উদাহরণ

নিম্নলিখিত উদাহরণটি [w3schools](https://www.w3schools.com/xml/xsl_intro.asp) থেকে নেওয়া হয়েছে৷
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## তথ্যসূত্র ##

* [XSLT - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/XSLT)

* [XSLT উপাদান](https://en.wikipedia.org/wiki/XSLT_elements)


