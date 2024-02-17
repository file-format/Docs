{
  "date" : "2021-08-29",
  "keywords" : [ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "ADE ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি ADE ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "ADE - এক্সেস প্রজেক্ট এক্সটেনশন ফাইল",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## একটি ADE ফাইল কি?

.ade এক্সটেনশন সহ একটি ফাইল হল একটি মাইক্রোসফ্ট অ্যাক্সেস প্রজেক্ট ফাইল যাতে Microsoft Access ADP প্রকল্প ফাইলে থাকা তথ্যের সংকলিত আউটপুট থাকে। ভিজ্যুয়াল বেসিক ফর অ্যাপ্লিকেশান (VBA) ব্যতীত অ্যাক্সেস প্রজেক্ট ফাইলের তথ্য ADE ফাইলগুলিতে সংকলিত আকারে পাওয়া যায়। ফাইলের আকার কমাতে এবং অ্যাক্সেসে কর্মক্ষমতা উন্নত করতে এই ফাইলগুলিতে ডেটা সংকুচিত বিন্যাসে সংরক্ষণ করা হয়। যেহেতু ADE হল Access প্রজেক্ট ফাইলের কম্পাইল করা আউটপুট, যেকোন VBA সোর্স কোড যা প্রজেক্টের অংশ, সেটিকে আউটপুটের অংশ হতে না দিয়ে সুরক্ষিত থাকে। ADE ফাইলগুলি Microsoft Access 365 এ খোলা যেতে পারে।

## ADE ফাইল ফরম্যাট - আরও তথ্য

ADE হল সংকলিত অ্যাক্সেস ডাটাবেস ফাইল যা ডিস্কে বাইনারি ফাইল হিসাবে সংরক্ষণ করা হয়। এই ফাইলগুলির অভ্যন্তরীণ ফাইল কাঠামো জানা নেই।

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. এই সমস্যাটি ঘটে কারণ Access 2010 SP1 VBE7.dll ফাইলের (সংস্করণ 7.00.1619) একটি নতুন সংস্করণ ব্যবহার করে।

## তথ্যসূত্র

* [এডিই ফাইল অ্যাক্সেসের সমস্যা](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [কোন অ্যাক্সেস ফাইল ফর্ম্যাটগুলি ব্যবহার করতে হবে](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


