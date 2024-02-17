{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM ফাইল ফরম্যাট - অ্যাসেম্বলি ল্যাঙ্গুয়েজ সোর্স কোড ফাইল ফরম্যাট",
  "description":"ASM ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা ASM ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-bn",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## একটি ASM ফাইল কি? ##

একটি ASM ফাইল হল নিম্ন স্তরের প্রোগ্রামিং ভাষায় লিখিত একটি প্রোগ্রাম যা সমাবেশ ভাষা হিসাবে পরিচিত। এটি প্রাথমিকভাবে হার্ডওয়্যার সম্পর্কিত কোড লেখার জন্য ব্যবহৃত হয় যেমন প্রোগ্রামিং মাইক্রো-কন্ট্রোলারের জন্য। প্রোগ্রামটি সহজ সমাবেশ ভাষা সিনট্যাক্স ব্যবহার করে লেখা হয় যাতে বিভিন্ন অপারেশন চালানোর জন্য অপারেটর এবং অপারেন্ড অন্তর্ভুক্ত থাকে। ASM ফাইল টেক্সট এডিটরগুলিতে লেখা ও সম্পাদিত হয় এবং HLA, MASM, FASM, NASM, বা GAS এর মতো অ্যাসেম্বলার প্রোগ্রাম ব্যবহার করে সম্পাদিত হয়।

## ASM ফাইল ফরম্যাট

ASM ফাইলগুলি **অবজেক্ট কোড** তৈরি করার জন্য একটি অ্যাসেম্বলার দ্বারা সঞ্চালিত হয় এমন অপারেশনগুলির একটি ক্রম নিয়ে গঠিত। ফলস্বরূপ অবজেক্ট কোড হল মেমোনিক্স এবং অ্যাড্রেসিং মোডগুলির সংমিশ্রণের একটি অনুবাদ যা তাদের সংখ্যাসূচক সমতুল্য।

### ASM ফাইল ফরম্যাটের উদাহরণ

x86 আর্কিটেকচারের জন্য **হ্যালো ওয়ার্ল্ড** অ্যাপ্লিকেশনের একটি উদাহরণ নিচে দেওয়া হল।
```
global  go
extern  _ExitProcess@4
extern  _GetStdHandle@4
extern  _WriteConsoleA@20

section .data
msg:    db      'Hello, World', 10
handle: db      0
written:
db      0

section .text
go:
; handle = GetStdHandle(-11)
push    dword -11
call    _GetStdHandle@4
mov     [handle], eax

; WriteConsole(handle, &msg[0], 13, &written, 0)
push    dword 0
push    written
push    dword 13
push    msg
push    dword [handle]
call    _WriteConsoleA@20

; ExitProcess(0)
push    dword 0
call    _ExitProcess@4
```

## রেফারেন্স ##

* [সমাবেশের ভাষা - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Assembly_language)

* [সমাবেশের ভাষা - মৌলিক সিনট্যাক্স](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


