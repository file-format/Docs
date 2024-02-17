{
  "date" : "2019-10-11",
  "keywords" : [ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASHX ফাইল এক্সটেনশন - একটি ASP.NET ওয়েব হ্যান্ডলার ফাইল",
  "description" : "একটি ASHX ফাইল এবং APIগুলি কী যেগুলি ASHX ফাইলগুলি তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## একটি ASHX ফাইল কি?

একটি ASHX ফাইল হল একটি ওয়েবপৃষ্ঠা যা ASP.NET HTTP হ্যান্ডলার দ্বারা ব্যবহারকারীকে এই ফাইলের ভিতরে উল্লেখ করা পৃষ্ঠাগুলির সাথে পরিবেশন করার জন্য ব্যবহার করা হয়। ASP.NET HTTP হ্যান্ডলার আগত অনুরোধ প্রক্রিয়া করে, .ashx ফাইল থেকে পৃষ্ঠাগুলি উল্লেখ করে এবং কম্পাইল করা পৃষ্ঠাটি ব্যবহারকারীর ব্রাউজারে ফেরত পাঠায়। প্রক্রিয়াকরণের পদ্ধতিটি বেশিরভাগ ASPX ফাইলের মতই ভিন্ন ভিন্ন যে এই ক্ষেত্রে, রেফারেন্স করা পৃষ্ঠা/নথিগুলি প্রক্রিয়া করা হয় এবং ফেরত পাঠানো হয়।

## ASHX ফাইল ফরম্যাট

.ashx ফাইলগুলি প্লেইন টেক্সট ফাইল ফরম্যাটে সংরক্ষিত হয় এবং এতে অন্যান্য পেজ বা ডকুমেন্টের রেফারেন্স থাকে যা অনুরোধের ভিত্তিতে ব্যবহারকারীর ব্রাউজারে ফেরত পাঠানো হয়। এগুলো যেকোন টেক্সট এডিটর এবং ডেভেলপার আইডিইতে খোলা যেতে পারে যেমন Xamarin স্টুডিও, মাইক্রোসফট নোটপ্যাড, নোটপ্যাড++ এবং আরও অনেক কিছু। ASHX ফাইলগুলি সেই ক্ষেত্রে দরকারী যখন আপনার কাছে থাকে:
 * বাইনারি ফাইল
 * ডায়নামিক ইমেজ ভিউ
 * কর্মক্ষমতা-সমালোচনামূলক ওয়েব পেজ
 * XML ফাইল
 * ন্যূনতম ওয়েব পেজ

## কিভাবে গতিশীলভাবে একটি ASHX ফাইল কম্পাইল করবেন?

মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও ব্যবহার করে একটি ASHX ফাইল যোগ এবং কম্পাইল করতে নিম্নলিখিত পদক্ষেপগুলি ব্যবহার করা যেতে পারে।

 * ভিজ্যুয়াল স্টুডিওতে একটি জেনেরিক হ্যান্ডলার যোগ করুন - Handler1.ashx
 * স্বয়ংক্রিয়ভাবে তৈরি cs ফাইলটি মুছুন।
 * আবার ashx খুলুন,
** CodeBehind=Handler1.ashx.cs সরান
** নিচে c# কোড যোগ করুন

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### ASHX উদাহরণ

ইন্টারনেট ব্রাউজারে ASHX ফাইল কল করা হলে নিম্নলিখিত ASHX কোডটি ব্যবহারকারীর অনুরোধে ইমেজ ফাইলটি ফেরত দেয়।


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  

using System;  
using System.Web;  

public class QueryStringHandler : IHttpHandler   
{  
    public void ProcessRequest (HttpContext context)   
    {  
        HttpResponse r = context.Response;  
        r.ContentType = "image/png";  
        string file = context.Request.QueryString["file"];  
        if (file == "Arrow")  
        {  
            r.WriteFile("Arrow.gif");  
        }  
        else  
        {  
            r.WriteFile("Image.gif");  
        }  
    }  

    public bool IsReusable   
    {  
        get  
        {  
            return false;  
        }  
    }  
}  
```

## তথ্যসূত্র

 * [ASHX ফাইল কম্পাইল করুন](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

