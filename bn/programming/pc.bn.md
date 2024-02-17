{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "পিসি ফাইল - প্রো*সি সোর্স কোড ফাইল - .pc ফাইল কি এবং কিভাবে খুলতে হয়?",
  "description" : "PC Pro*C সোর্স কোড ফাইল এবং এটি কিভাবে খুলতে হয় সে সম্পর্কে জানুন।",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-bn",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## একটি পিসি ফাইল কি?

PC ফাইল বা .pc ফাইল হল একটি ProC সোর্স কোড ফাইল। ProC হল একটি প্রি-কম্পাইলার যা ওরাকল ডাটাবেসের সাথে সি বা সি++ কোডের মধ্যে এসকিউএল স্টেটমেন্ট এম্বেড করতে ব্যবহৃত হয়। আপনি যখন Pro*C ফাইল কম্পাইল করেন, তখন এটি এমবেডেড SQL কমান্ড সহ নিয়মিত C বা C++ কোড তৈরি করে। এটি আপনাকে আপনার C বা C++ প্রোগ্রামগুলির সাথে নির্বিঘ্নে SQL ডাটাবেস অপারেশনগুলিকে একীভূত করতে দেয়।

প্রো*সি ফাইলটি দেখতে কেমন হতে পারে তার প্রাথমিক উদাহরণ এখানে রয়েছে:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

এই উদাহরণে, এসকিউএল স্টেটমেন্টগুলিকে EXEC SQL এর সাথে প্রিফিক্স করা হয়েছে যাতে বোঝা যায় যে সেগুলি এম্বেড করা SQL স্টেটমেন্ট। এই বিবৃতিগুলি প্রো*সি প্রিকম্পাইলার দ্বারা প্রক্রিয়া করা হবে যখন ফাইল কম্পাইল করা হবে এবং ওরাকল ডাটাবেসের সাথে ইন্টারঅ্যাক্ট করার জন্য উপযুক্ত সি কোড তৈরি করা হবে।

## কিভাবে পিসি ফাইল খুলবেন?

একটি পিসি ফাইল খুলতে, আপনার সাধারণত একটি পাঠ্য সম্পাদক বা একটি ইন্টিগ্রেটেড ডেভেলপমেন্ট এনভায়রনমেন্ট (IDE) প্রয়োজন যা C বা C++ সোর্স কোড সম্পাদনা সমর্থন করে। এখানে কিছু সাধারণ বিকল্প রয়েছে:

1.  **টেক্সট এডিটর:**
    
- **নোটপ্যাড** (উইন্ডোজ)
- **টেক্সট এডিট** (ম্যাক)
- **gedit** (লিনাক্স)
- **সাবলাইম টেক্সট**
- **পরমাণু**
- **ভিজ্যুয়াল স্টুডিও কোড**
2.  **ইন্টিগ্রেটেড ডেভেলপমেন্ট এনভায়রনমেন্ট (IDEs):**
    
- CDT (C/C++ ডেভেলপমেন্ট টুলিং) সহ **Eclipse**
- **ভিজ্যুয়াল স্টুডিও** ভিজ্যুয়াল সি++ সহ বা সি++ এক্সটেনশন সহ ভিজ্যুয়াল স্টুডিও কোড
- **কোড::ব্লক**
- C/C++ প্যাক সহ **NetBeans**
  
## তথ্যসূত্র
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


