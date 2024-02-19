{
  "date": "2021-05-20",
  "keywords": [
    "stml",
    "stml file",
    "stml file format",
    "stml file type",
    "file",
    "type",
    "what is an stml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "STML - SSI HTML ফাইল",
  "description": "STML ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি STML ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stml-bn"
    }
  },
  "lastmod": "2021-05-20"
}

## একটি STML ফাইল কি?

.stml এক্সটেনশন সহ একটি ফাইল হল সার্ভার সাইড নির্দেশাবলী সহ একটি ওয়েবপৃষ্ঠা যা ব্যবহারকারী যখন ওয়েব ব্রাউজারে পৃষ্ঠাটি লোড করে তখন কার্যকর করা হয়। STML পৃষ্ঠাগুলিতে সার্ভার সাইড কোড থাকে যা সার্ভার সাইড ধারণ করে এমন কাজগুলি সম্পাদন করে যা প্লেইন HTML দিয়ে অর্জন করা সম্ভব নয়। যদিও [HTML](/web/html/)-এর মতো, STML সার্ভারে কমান্ডগুলি চালানোর মাধ্যমে আরও শক্তি সরবরাহ করে, যাকে সার্ভার সাইড ইনক্লুডস (SSI)ও বলা হয়। PHP-এর মতো সার্ভার সাইড স্ক্রিপ্টিং সহ নতুন প্রোগ্রামিং ভাষার প্রবর্তনের সাথে, STML এর ব্যবহার হ্রাস পেয়েছে যদিও এটি এখনও সমস্ত সার্ভার সাইড প্রযুক্তি দ্বারা সমর্থিত। STML ফাইলগুলি যেকোনো টেক্সট এডিটরে খোলা যায় এবং কমান্ড আপডেট করার জন্য এডিট করা যায়।

## STML ফাইল ফরম্যাট

STML সাধারণ ascii টেক্সট ফাইল ফরম্যাটের উপর ভিত্তি করে যা মানুষের পাঠযোগ্য। যাইহোক, এটি সার্ভার সাইডে সম্পাদিত [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) ব্যবহার করে সংজ্ঞায়িত এবং অনুশীলন করা সিনট্যাক্স অনুসরণ করে। অন্য যেকোনো সার্ভার সাইড স্ক্রিপ্টিং ভাষার মতো, STML সার্ভার সাইড কমান্ড ব্যবহার করতে পারে যেমন পেজ ভিজিটর কাউন্টার, ওয়েব পেজ ক্যালেন্ডার, ডাটাবেস থেকে রেকর্ড পুনরুদ্ধার করা এবং অনুরূপ অন্যান্য কাজ করতে।

## STML উদাহরণ

সার্ভার সাইড নির্দেশাবলী পৃষ্ঠা ভিজিটর কাউন্টার বা ওয়েব পৃষ্ঠা ক্যালেন্ডারের মতো অ্যাপ্লিকেশনগুলিতে ব্যবহৃত হয়। নিম্নলিখিত উদাহরণ, ব্যবহারকারীদের ডাটাবেসের প্রথম তিনটি লাইনের প্রথম চারটি কলাম প্রদর্শন করে।

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## তথ্যসূত্র

* [সার্ভার সাইড অন্তর্ভুক্ত](https://en.wikipedia.org/wiki/Server_Side_Includes)


