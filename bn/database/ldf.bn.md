{
  "date" : "2020-11-11",
  "keywords" : [ "LDF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "LDF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি LDF ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title" : "LDF - SQL সার্ভার মাস্টার ডাটাবেস ফাইল ফরম্যাট",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## একটি LDF ফাইল কি?

.ldf এক্সটেনশন সহ একটি ফাইল মাইক্রোসফ্ট এসকিউএল সার্ভার দ্বারা রক্ষণাবেক্ষণ করা একটি লগ ফাইল যা একটি রিলেশনাল ডাটাবেস ম্যানেজমেন্ট সিস্টেম (RDBMS)। প্রাথমিক ডাটাবেস ফাইলে ([MDF](/database/mdf/)) (যেমন সন্নিবেশ, আপডেট, মুছে ফেলা) সম্পাদিত সমস্ত লেনদেন LDF ফাইলে রেকর্ড করা হয়। LDF ফাইল যে কোনো ডাটাবেসের গুরুত্বপূর্ণ উপাদান। একটি সিস্টেম ব্যর্থতার ক্ষেত্রে, লগ ফাইলটি ডাটাবেসটিকে একটি সামঞ্জস্যপূর্ণ অবস্থায় পুনরুদ্ধার করতে ব্যবহৃত হয়। লেনদেন সম্পূর্ণরূপে প্রতিশ্রুতিবদ্ধ না হলে লেনদেনের লগ ফাইলের আকার বাড়তে পারে। মাইক্রোসফ্ট এসকিউএল সার্ভার সফ্টওয়্যার অ্যাপ্লিকেশন দিয়ে LDF ফাইলগুলি খোলা যেতে পারে।

## LDF ফাইলে রেকর্ডকৃত অপারেশন

একটি SQL লগ ফাইল নিম্নলিখিত ক্রিয়াকলাপগুলি রেকর্ড করে:

 * প্রতিটি লেনদেনের শুরু এবং শেষ।

 * প্রতিটি ডেটা ডেটা পরিবর্তন (সন্নিবেশ করা, আপডেট করা বা মুছে ফেলা)। এর মধ্যে সিস্টেম সারণী সহ যেকোনো টেবিলে সিস্টেম সঞ্চিত পদ্ধতি বা ডেটা ডেফিনিশন ল্যাঙ্গুয়েজ (DDL) স্টেটমেন্টের পরিবর্তনও অন্তর্ভুক্ত রয়েছে।

 * প্রতিটি ব্যাপ্তি এবং পৃষ্ঠা বরাদ্দ বা ডিলোকেশন।

 * একটি টেবিল বা সূচক তৈরি বা ড্রপ করা।

## LDF ফাইল ফরম্যাট

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. যেহেতু ক্রিয়াকলাপগুলি একটি সিরিয়ালে রেকর্ড করা হয়েছে, LSN2 দ্বারা বর্ণিত পরিবর্তনটি লগ রেকর্ড LSN1 এর পরে সঞ্চালিত হয়েছিল। একটি নির্দিষ্ট লেনদেনের রেকর্ডগুলি ব্যবহার করা পয়েন্টারগুলি ব্যবহার করে পিছনের দিকে লিঙ্ক করা হয় এবং লেনদেনের রোলব্যাককে গতি দেয়।
 
## তথ্যসূত্র

 * [ডেটাবেস ফাইল এবং ফাইলগ্রুপ](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [লেনদেন লগ আর্কিটেকচার এবং ম্যানেজমেন্ট গাইড](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -ভার15)

