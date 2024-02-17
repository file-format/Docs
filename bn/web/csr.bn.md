{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR ফাইল - সার্টিফিকেট সাইনিং রিকোয়েস্ট ফাইল ফরম্যাট",
  "description" : "একটি সিএসআর ফাইল এবং এপিআই কী সে সম্পর্কে জানুন যা সিএসআর ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-bn",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## একটি CSR ফাইল কি?

একটি CSR ফাইল হল একটি **শংসাপত্র স্বাক্ষরের অনুরোধ** ফাইল যা SSL/TLS শংসাপত্রের জন্য অনুরোধ করতে ব্যবহৃত হয়। যখন আপনার SSL/TLS শংসাপত্রের প্রয়োজন হয়, আপনি একই সার্ভারে CSR তৈরি করেন যেখানে এটি অবশেষে ইনস্টল করা হবে। সার্টিফিকেট তৈরির জন্য এই CSR ফাইলটি সার্টিফিকেট অথরিটি (CA) এর সাথে শেয়ার করা হয়েছে। এটিতে সাধারণ নাম, সংস্থা, দেশ এবং আরও গুরুত্বপূর্ণভাবে, **পাবলিক কী** এর মতো তথ্য রয়েছে যা আপনার শংসাপত্র ফাইলের মধ্যে একত্রিত এবং সংশ্লিষ্ট ব্যক্তিগত কী দিয়ে স্বাক্ষরিত।

যেসব অ্যাপ্লিকেশন **CSR ফাইল খুলতে পারে** সেগুলির মধ্যে OpenSSL এবং Microsoft IIS অন্তর্ভুক্ত রয়েছে।

## শংসাপত্র স্বাক্ষর অনুরোধ ফাইল বিন্যাস

একটি CSR ফাইল একটি বেস-64 পিইএম ফরম্যাটে তৈরি করা হয় যা মাইক্রোসফ্ট নোটপ্যাডের মতো সাধারণ পাঠ্য সম্পাদকে খোলা এবং দেখা যায়। এতে একটি শিরোনাম রয়েছে --------- নতুন শংসাপত্রের অনুরোধ শুরু করুন -----** ফাইলের শুরুতে এবং একটি ফুটার **------ শেষ নতুন শংসাপত্রের অনুরোধ--------- ফাইলের শেষ।

### একটি CSR ফাইল দেখতে কেমন?

একটি CSR ফাইলের একটি সাধারণ উদাহরণ অনুসরণ করা হল।

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## কোন তথ্য একটি CSR অন্তর্ভুক্ত করা হয়?

একটি CSR ফাইলে নিম্নলিখিত তথ্য রয়েছে।

1. `ব্যবসা এবং ওয়েবসাইট সম্পর্কে তথ্য` - সাধারণ নাম, সংস্থা, সাংগঠনিক ইউনিট, শহর/স্থানীয়, রাজ্য/কাউন্টি/অঞ্চল (এস), দেশ এবং ইমেল ঠিকানার মতো তথ্য অন্তর্ভুক্ত করে
1. পাবলিক কী' - এটি শংসাপত্রের মধ্যে অন্তর্ভুক্ত করা হয় এবং প্রেরিত ডেটা এনক্রিপ্ট করতে ব্যবহৃত হয় যা সংশ্লিষ্ট ব্যক্তিগত কী ব্যবহার করে ডিক্রিপ্ট করা হয়
1. `কি টাইপ এবং দৈর্ঘ্য সম্পর্কে তথ্য` - এটি সাধারণত RSA 2048 হয় তবে RSA 4096+ এর মতো বড় আকারেও আসতে পারে

## তথ্যসূত্র

* [কনসেপ্ট অ্যাপ্লিকেশন সার্ভার](https://github.com/Devronium/ConceptApplicationServer)


