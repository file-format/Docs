{
  "date": "2021-04-22",
  "keywords": [
    ".pas file",
    "pas file format",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "PAS - ডেলফি ইউনিট সোর্স ফাইল",
  "description": "PAS উদাহরণ সহ PAS ফাইল বিন্যাস সম্পর্কে জানুন এবং এপিআইগুলি যা PAS ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pas-bn"
    }
  },
  "lastmod": "2021-04-22"
}

## একটি PAS ফাইল কি?
একটি .pas ফাইল আসলে একটি সোর্স কোড ফাইল যা একটি ডেলফি প্রোগ্রামিং প্রকল্পে পাওয়া যায়। ডেলফি হল একটি সফটওয়্যার ডেভেলপমেন্ট অ্যাপ্লিকেশন যা ডেভেলপাররা উইন্ডোজ ভিত্তিক সফ্টওয়্যার তৈরির জন্য ব্যবহার করে; ডেলফি ভাষায় লেখা। ডেলফি ভাষা হল অবজেক্ট প্যাসকেল ভাষার একটি রূপ। তাই এটি ডেলফি কম্পাইলারের সাথে নেটিভ Win32 কোডে কম্পাইল করা যেতে পারে।

## PAS ফাইল বিন্যাস

PAS ফাইল ফরম্যাট হল একটি কোডিং ফাইল যা ডেলফি ইউনিট উৎসের জন্য সংরক্ষিত। ইউনিটগুলি ডেলফি অ্যাপের প্রধান বিল্ডিং ব্লক হিসাবে উপলব্ধি করা হয়। আপনি বর্তমান ডেলফি প্রকল্পের সোর্স কোড **প্রকল্প > উৎস দেখুন** মেনুর মাধ্যমে দেখতে পারেন। প্রোগ্রামাররা একটি ইউনিট তৈরি করতে এবং একটি স্বতন্ত্র ফাইল হিসাবে সংরক্ষণ করতে পারে যা যেকোনো প্রকল্প ব্যবহার করতে পারে। একবার প্রকল্পে একটি ইউনিট যোগ করা হলে, ডেলফি এটিকে প্রকল্পের .DPR ফাইলের ব্যবহার ধারায় নিবন্ধন করে।

## PAS ফাইলের উদাহরণ
যখন আমরা কোডের একটি লাইন লিখি। ডেলফি আমাদের জন্য বুদ্ধিমত্তার সাথে অনেক লাইন লেখেন। সমস্ত সোর্স কোড PAS ফাইলে লেখা আছে। নিম্নলিখিত ডেলফি সোর্স ইউনিট বা PAS ফাইলের একটি মৌলিক উদাহরণ:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## তথ্যসূত্র

 * [ডেলফি প্রকল্প এবং ইউনিট সোর্স ফাইলগুলি বোঝা](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [আপনার প্রথম ডেলফি প্রোগ্রাম লেখা](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

