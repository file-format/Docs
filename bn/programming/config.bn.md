{
  "date": "2021-04-23",
  "keywords": [
    "config File",
    "configuration files",
    "config File format",
    "extension",
    "format",
    "git config file",
    "Configuration files in Linux",
    "what is a config file",
    "Config file php",
    "ssh config file example",
    "aws config file example",
    "python config file example"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "CONFIG - কনফিগারেশন ফাইল",
  "description": "CONFIG উদাহরণ সহ CONFIG ফাইল বিন্যাস সম্পর্কে জানুন এবং API গুলি যা CONFIG ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-config-bn"
    }
  },
  "lastmod": "2021-04-23"
}

## কনফিগ ফাইল কি?
একটি CONFIG ফাইল কনফিগারেশন ফাইল হিসাবে পরিচিত; বিভিন্ন কম্পিউটার সফ্টওয়্যারের জন্য প্যারামিটার এবং প্রাথমিক সেটিংস কনফিগার করতে ব্যবহৃত হয়। কিছু সফ্টওয়্যার তাদের স্টার্টআপে শুধুমাত্র তাদের **কনফিগারেশন ফাইল** পড়ে। অন্যরা পর্যায়ক্রমে পরিবর্তনের জন্য কনফিগারেশন ফাইলগুলি পরীক্ষা করে।

## কনফিগ ফাইল ফরম্যাট
**কনফিগ ফাইল ফরম্যাট** সার্ভার প্রক্রিয়া, সফ্টওয়্যার অ্যাপ্লিকেশন, এবং অপারেটিং সিস্টেম সেটিংসের জন্য ব্যবহৃত হয়। একটি প্রোগ্রামার নির্দিষ্ট সময়ের পরে কনফিগারেশন ফাইলগুলি বারবার পড়তে এবং বর্তমান প্রক্রিয়ায় পরিবর্তনগুলি প্রয়োগ করার জন্য একটি সফ্টওয়্যারকে নির্দেশ দেওয়ার জন্য কোড লিখতে পারে। কনফিগ ফাইল সিন্সট্যাক্সের জন্য কোন নির্দিষ্ট মান বা শক্তিশালী নিয়ম নেই। উদাহরণস্বরূপ, Microsoft-এর Web.config ফাইলটি CONFIG ফাইল ফরম্যাটের অন্তর্গত, যা একটি [XML](/web/xml/) ভিত্তিক ট্যাগসেট নিয়ে গঠিত; Microsoft Visual Studio বা অন্য কোন টেক্সট এডিটর দিয়ে সম্পাদনা করা যেতে পারে।

## কনফিগারেশন ফাইলের উদাহরণ:
যেহেতু, কনফিগারেশন ফাইলগুলি কোনও নিয়ম, স্ট্যান্ড্রাড বা নিয়ম অনুসরণ করে তৈরি করা হয় না, তাই এই ফাইলগুলি বিভিন্ন বিন্যাস ব্যবহার করে লেখা হতে পারে। একটি .config ফাইল XML, [JSON](/web/json/) বা অন্য কোনো ফর্ম্যাটের উপর ভিত্তি করে হতে পারে। সুপরিচিত অপারেটিং সিস্টেম এবং সফ্টওয়্যারগুলির জন্য কনফিগারেশন ফাইলগুলির উদাহরণ নিম্নরূপ:

### লিনাক্সে কনফিগারেশন ফাইল
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|বিভাগ |উদাহরণ | মন্তব্য|
---|---|---|
|অ্যাক্সেস ফাইল|/etc/host.conf|নেটওয়ার্ক ডোমেইন সার্ভারকে বলে কিভাবে হোস্টনাম দেখতে হয়।|
|বুটিং এবং লগইন/logout|/etc/rc.d/rc.local|অফিসিয়াল নয়৷ rc, rc.sysinit, অথবা /etc/inittab.| থেকে কল করা যেতে পারে
|ফাইল সিস্টেম|/etc/mtools.conf|একটি DOS-টাইপ ফাইল সিস্টেমে সমস্ত অপারেশনের (mkdir, কপি, বিন্যাস, ইত্যাদি) কনফিগারেশন৷|
সিস্টেম প্রশাসন
|নেটওয়ার্কিং|/etc/gated.conf|গেটেডের জন্য কনফিগারেশন। শুধুমাত্র গেটেড ডেমন দ্বারা ব্যবহৃত.|
|সিস্টেম কমান্ড|/etc/logrotate.conf|ডাইনামিক লিঙ্কারের জন্য কনফিগারেশন।|
|Daemons|/etc/httpd.conf|অ্যাপাচি, ওয়েব সার্ভারের জন্য কনফিগারেশন ফাইল। এই ফাইলটি সাধারণত /etc.|-এ থাকে না
|ব্যবহারকারী প্রোগ্রাম| /etc/lynx.cfg| প্রক্সি সেটিংস|
### AWS CONFIG ফাইলের উদাহরণ
ঘন ঘন ব্যবহৃত কনফিগারেশন সেটিংস এবং শংসাপত্রগুলি কনফিগ ফাইলগুলিতে সংরক্ষণ করা যেতে পারে যা AWS CLI দ্বারা রক্ষণাবেক্ষণ করা হয়। CONFIG ফাইলটি অবশ্যই একটি প্লেইনটেক্সট ফাইল হতে হবে যা নিম্নলিখিত ফর্ম্যাট ব্যবহার করে:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG ফাইলের উদাহরণ
OpenSSH ক্লায়েন্ট-সাইড কনফিগারেশন ফাইলের নাম CONFIG, এবং এটি .ssh ডিরেক্টরিতে সংরক্ষণ করা হয়। SSH CONFIG ফাইলটি নিম্নলিখিত কাঠামো নিয়ে গঠিত:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### পাইথন কনফিগ ফাইলের উদাহরণ
একটি Python CONFIG ফাইল এই মত দেখতে পারে:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## তথ্যসূত্র

 * [লিনাক্স কনফিগারেশন ফাইল বোঝা](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [পাইথনে কনফিগারেশন ফাইল](https://martin-thoma.com/configuration-files-in-python/)

