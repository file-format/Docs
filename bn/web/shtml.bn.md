{
  "date": "2021-05-20",
  "keywords": [
    "shtml",
    "shtml file",
    "shtml file format",
    "shtml file type",
    "file",
    "type",
    "what is an shtml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "SHTML - সার্ভার সাইড HTML ফাইল অন্তর্ভুক্ত করুন",
  "description": "এসএইচটিএমএল ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা এসএইচটিএমএল ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtml-bn"
    }
  },
  "lastmod": "2021-05-20"
}

## একটি SHTML ফাইল কি?

.shtml এক্সটেনশন সহ একটি ফাইল হল একটি ওয়েবপৃষ্ঠা যা [HTML](/web/html/)-এ লেখা এবং সার্ভারের নির্দেশাবলী অন্তর্ভুক্ত৷ এটিতে দ্রুত লোড করার জন্য ASP ফাইলের মতো সার্ভার-সাইড অন্তর্ভুক্ত থাকতে পারে। সার্ভার সাইড ফাইলগুলিতে এক্সিকিউটেবল কোডও থাকতে পারে যা সার্ভারটিকে স্বাভাবিকের চেয়ে ধীর লোড করতে পারে। এসএইচটিএমএল ফাইলগুলি এইচটিএমএল এর অনুরূপ তবে তারা সাধারণ সার্ভার কমান্ড ব্যবহারের অনুমতি দেয়। এই সার্ভার কমান্ডগুলি সার্ভার সাইড ইনক্লুডস (SSI) নামে একটি সাধারণ কম্পিউটার প্রোগ্রামিং ভাষায় সঞ্চালিত হয়। অন্যান্য সার্ভার সাইড প্রোগ্রামিং ল্যাঙ্গুয়েজ যেমন [PHP](/programming/php/) অন্তর্ভুক্ত করে SHTML-এর স্থগিত করা হয়েছে।

## SHTML ফাইল ফরম্যাট

SHTML ফাইলগুলি প্লেইন টেক্সটে লেখা হয় এবং সার্ভার সাইডে কার্যকর করা [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) ব্যবহার করে। এই সার্ভার সাইড কমান্ড ডাটাবেস ড্রাইভার ব্যবহার করে ডাটাবেসের সাথে সংযোগ করতে এবং টেবিল থেকে ব্যবহারকারীদের ডেটা আনতে ব্যবহার করা যেতে পারে।

## SHTML উদাহরণ

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


