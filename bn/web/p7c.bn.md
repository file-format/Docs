{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "P7C - PKCS 7 সার্টিফিকেট ফাইল",
  "description":"P7C ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি P7C ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## একটি P7C ফাইল কি?

একটি P7C ফাইল, অন্যান্য নিরাপত্তা শংসাপত্র ফাইলগুলির মতো, একটি ডিজিটাল শংসাপত্র যা নেটওয়ার্কের মাধ্যমে পরিচয় প্রমাণীকরণ করতে ব্যবহৃত হয়। শংসাপত্র ব্যবহার করে অ্যাপ্লিকেশনগুলি এই সার্টিফিকেট ফাইলগুলিতে অন্তর্ভুক্ত সর্বজনীন কী ব্যবহার করে পরিচয় প্রমাণীকরণ করে। পাবলিক-কী ক্রিপ্টোগ্রাফি, বা অ্যাসিমেট্রিক ক্রিপ্টোগ্রাফি, কীগুলির জোড়া ব্যবহার করে যার একটি সর্বজনীন কী এবং অন্যটি ব্যক্তিগত কী হিসাবে পরিচিত। ব্যক্তিগত কী কার্যকর নিরাপত্তার জন্য সুরক্ষিত রাখা হয়, যখন সর্বজনীন কী অন্যদের সাথে ভাগ করা যায়। অন্যান্য সাধারণ সার্টিফিকেট ফাইল ফরম্যাটের মধ্যে রয়েছে [CRT](/web/crt/), DER, এবং PEM।

## P7C ফাইল ফরম্যাট - আরও তথ্য

P7C ফাইলগুলি বাইনারি ফাইল হিসাবে ডিস্কে সংরক্ষণ করা হয় এবং গাণিতিক সমস্যার উপর ভিত্তি করে ক্রিপ্টোগ্রাফিক অ্যালগরিদম ব্যবহার করে তৈরি করা সর্বজনীন কী তথ্য অন্তর্ভুক্ত করে। এগুলি যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে তবে তাদের বিষয়বস্তু মানুষের পাঠযোগ্য আকারে নয়। P7C ফাইল খুলতে পারে এমন কিছু অ্যাপ্লিকেশনের মধ্যে রয়েছে Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager, এবং Microsoft Windows Contacts।

### P7C ফাইল ফরম্যাটের উদাহরণ

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## তথ্যসূত্র ##

* [পাবলিক কী ক্রিপ্টোগ্রাফি](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [কিভাবে P7C ফাইল তৈরি করবেন?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


