{
  "date" : "2021-06-28",
  "keywords" : [ "cgi file", "what is a cgi file", "file", "cgi example", "cgi file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CGI ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CGI ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "CGI - সাধারণ গেটওয়ে ইন্টারফেস স্ক্রিপ্ট ফাইল",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## একটি CGI ফাইল কি?
একটি CGI ফাইল একটি সাধারণ গেটওয়ে ইন্টারফেস স্ক্রিপ্ট হিসাবে পরিচিত যা একটি ওয়েব সার্ভার ব্যবহারকারীর অনুরোধগুলি প্রক্রিয়া করার জন্য একটি বহিরাগত প্রোগ্রাম চালানোর জন্য ব্যবহার করে। .cgi এক্সটেনশন সহ একটি ফাইলে সংরক্ষিত স্ক্রিপ্ট সাধারণত সি বা পার্ল প্রোগ্রামিং ভাষায় লেখা হয়। ওয়েবের প্রথম দিন থেকে চালু করা হয়েছিল, যখন ওয়েব ডেভেলপাররা তাদের ওয়েব সার্ভারের সাথে ডাটাবেস সংযোগ করতে চেয়েছিল। একটি সার্ভার যা ওয়েব সার্ভার এবং ডাটাবেসের মধ্যে একটি সাধারণ গেটওয়ে সমর্থন করে তা সিজিআই কোড চালানোর জন্য উপযুক্ত ছিল।

## CGI ফাইল ফরম্যাট
CGI স্ক্রিপ্টগুলি ওয়েব সার্ভার দ্বারা ব্যবহার করা হয় যাতে একটি URL কীভাবে পরিচালনা করা হবে তা কনফিগার করতে মালিককে সুবিধা দেয়৷ পদ্ধতিটি সাধারণত সিজিআই স্ক্রিপ্ট ধারণকারী হিসাবে একটি নতুন ডিরেক্টরি (যেখানে নথি প্রধানত অবস্থিত) চিহ্নিত করে করা হয়; এর সাধারণ পরিচিত নাম সিজিআই-বিন। উদাহরণস্বরূপ, /usr/local/apache/htdocs/cgi-bin ওয়েব সার্ভারে একটি CGI ডিরেক্টরি হিসাবে বাছাই করা যেতে পারে। যখন একটি ওয়েব ব্রাউজার একটি URL অনুরোধ করে যা CGI ডিরেক্টরির মধ্যে একটি ফাইল নির্দেশ করে, তখন, সেই ফাইলটি (/usr/local/apache/htdocs/cgi-bin/printenv.pl) ওয়েব ব্রাউজারে পাঠানোর পরিবর্তে, HTTP সার্ভার নির্দিষ্ট স্ক্রিপ্ট চালায় এবং ওয়েব ব্রাউজারে স্ক্রিপ্টের আউটপুট ফেরত দেয়। সংক্ষেপে, CGI স্ক্রিপ্ট যা স্ট্যান্ডার্ড আউটপুটে পাঠানো হয় তা উইন্ডোর টার্মিনালে দেখানোর পরিবর্তে ওয়েব ক্লায়েন্টে স্থানান্তরিত হয়।

### CGI উদাহরণ

পার্লে লেখা CGI স্ক্রিপ্ট অনুসরণ করে যা ওয়েব সার্ভার দ্বারা পাস করা সমস্ত পরিবেশের ভেরিয়েবল দেখায়:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

আউটপুট নিম্নলিখিত মত হবে:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## CGI স্ক্রিপ্টের ব্যবহার
CGI স্ক্রিপ্ট ধারণকারী CGI ফাইলগুলি সাধারণত ব্যবহারকারীর কাছ থেকে ইনপুট ডেটা প্রক্রিয়া করতে এবং প্রাসঙ্গিক আউটপুট ডেটা তৈরি করতে ব্যবহৃত হয়। একটি উইকি বাস্তবায়ন CGI প্রোগ্রামের উদাহরণগুলির মধ্যে একটি। যদি ব্যবহারকারী এজেন্ট একটি এন্ট্রির নামের জন্য একটি অনুরোধ পাঠায়, ওয়েব সার্ভার CGI প্রোগ্রাম চালায়। CGI প্রোগ্রাম সেই এন্ট্রির পৃষ্ঠার উৎস পায়, এটিকে HTML-এ রূপান্তর করে এবং ফলাফল প্রিন্ট করে। ওয়েব সার্ভার CGI প্রোগ্রাম থেকে আউটপুট গ্রহণ করে এবং ব্যবহারকারী এজেন্টকে ফেরত দেয়। তারপর, যদি ব্যবহারকারী এজেন্ট পৃষ্ঠা সম্পাদনা করুন বোতামে ক্লিক করে সম্পাদনা ফাংশনকে কল করে, CGI প্রোগ্রামটি একটি HTML টেক্সটেরিয়া বা পৃষ্ঠার বিষয়বস্তু সহ অন্যান্য সম্পাদনা নিয়ন্ত্রণ দেখায়। অবশেষে, ব্যবহারকারী এজেন্ট যদি পৃষ্ঠা প্রকাশ করুন বোতামে ক্লিক করে, CGI প্রোগ্রাম আপডেট করা HTML-কে সেই এন্ট্রির পৃষ্ঠার উৎসে রূপান্তর করে এবং সংরক্ষণ করে।



## তথ্যসূত্র 

* [সাধারণ গেটওয়ে ইন্টারফেস - উইকিপিউডিয়া দ্বারা](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


