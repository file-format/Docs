{
  "date" : "2020-01-10",
  "keywords" : [ "dib file", "dib file format", "what is a dib file", "file", "dib example", "dib file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ডিআইবি",
  "description":"Learn about ডিআইবি file format and APIs that can create and open ডিআইবি files.",
  "linktitle" : "ডিআইবি",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## একটি ডিআইবি ফাইল কি?

একটি ডিভাইস-ইন্ডিপেন্ডেন্ট বিটম্যাপ (ডিআইবি) হল একটি রাস্টার ইমেজ ফাইল যা স্ট্যান্ডার্ড বিটম্যাপ ফাইলের ([BMP]()/image/bmp/)) কাঠামোর অনুরূপ। এটিতে একটি রঙের টেবিল রয়েছে যা পিক্সেল মানগুলিতে RGB রঙের ম্যাপিং বর্ণনা করে। এটি ডিআইবি কে যেকোনো ডিভাইসে চিত্র উপস্থাপন করতে সক্ষম করে। এটি প্রায় সমস্ত অ্যাপ্লিকেশনের সাথে খোলা যেতে পারে যা উইন্ডোজের পাশাপাশি ম্যাকওএস-এ একটি স্ট্যান্ডার্ড BMP ফাইল খুলতে পারে। ডিআইবি হল বাইনারি ফাইল এবং BMP এর মতই একটি জটিল ফাইল ফরম্যাট রয়েছে। ডিআইবি চিত্রগুলি রঙের গভীরতা এবং পিক্সেল-প্রতি-ইঞ্চির পরিপ্রেক্ষিতে রেন্ডারিং ডিভাইসের আউটপুট ক্ষমতা থেকে স্বাধীন।

## ডিআইবি ফাইল ফরম্যাট স্পেসিফিকেশন ##
একটি ডিআইবি নিম্নলিখিত রঙ এবং মাত্রা তথ্য ধারণ করে:

  * যে ডিভাইসে আয়তক্ষেত্রাকার ছবি তৈরি করা হয়েছিল তার রঙের বিন্যাস।
  * যে ডিভাইসে আয়তক্ষেত্রাকার ছবি তৈরি করা হয়েছিল তার রেজোলিউশন।
  * যে ডিভাইসে ছবিটি তৈরি করা হয়েছিল তার জন্য প্যালেট।
  * বিটগুলির একটি অ্যারে যা আয়তক্ষেত্রাকার ছবিতে লাল, সবুজ, নীল (RGB ) ট্রিপলেটকে পিক্সেল থেকে ম্যাপ করে৷
  * একটি ডেটা-কম্প্রেশন শনাক্তকারী যা বিটগুলির অ্যারের আকার কমাতে ব্যবহৃত ডেটা কম্প্রেশন স্কিম (যদি থাকে) নির্দেশ করে।

### ডিআইবি ডেটা ব্লক ফরম্যাট ###

ডিস্কে সংরক্ষিত .ডিআইবি ফাইলের তুলনায় ডিআইবি মেমরি ব্লকের প্রসঙ্গে আসে। মেমরি ব্লকের মধ্যে রয়েছে কাঠামো যা ডিআইবি-এর জন্য Windows API স্পেসিফিকেশন অনুসারে। প্রকৃত ডিআইবি এর মধ্যে রয়েছে:
  * একটি হেডার
  * রঙ্গের পাত
  * পিক্সেল ডেটা

কার্যত, প্যালেট, হেডার এবং ইমেজ ডেটার সাথে কাজ করা হয় যেন সেগুলি মেমরির তিনটি পৃথক ব্লক। মেমরির এই সাধারণ ব্লকের একটি হ্যান্ডেল GlobalAlloc ব্যবহার করে বরাদ্দ করা হয় এবং এটি Hডিআইবি নামে পরিচিত, যা হেডার, রঙ টেবিল এবং পিক্সেল ডেটা বের করতে এবং কাজ করতে ব্যবহৃত হয়।

### কাঠামো ###
একটি ডিআইবি তে থাকা তথ্য বিভিন্ন কাঠামো দ্বারা প্রতিনিধিত্ব করা হয়। এর মধ্যে রয়েছে:

BITMAInfo - একটি ডিআইবি-এর জন্য মাত্রা এবং রঙের তথ্য সংজ্ঞায়িত করে
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
এটি একটি BITMAPINFOHEADER নিয়ে গঠিত:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
দুই বা ততোধিক RGBQAD কাঠামো অনুসরণ করে।

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### ডেটা বিট ###
|বিটস|বর্ণনা|
---|---|
|1-বিট ফরম্যাট (একরঙা)|একরঙা বিটম্যাপ দুটি রঙ (কালো এবং সাদা) নিয়ে গঠিত। এই সীমিত সংখ্যক রঙের কারণে, এই বিটম্যাপগুলি ডিস্কে কম জায়গা নেয়। bitBitCount উভয় রঙের প্রতিনিধিত্বের জন্য সত্য বা মিথ্যা ফেরত দেয়। bitBitCount==1 হলে বেশিরভাগ অ্যাপ্লিকেশন প্যালেটটি সম্পূর্ণভাবে এড়িয়ে যায়।
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. এই বিটগুলি পিক্সেলের রঙকে অবতরণ ক্রমে উপস্থাপন করে।
|8 বিট বিন্যাস (256 রঙ)|এই 8-বিট বিন্যাসটি সর্বাধিক 256টি রঙের প্রতিনিধিত্ব করতে পারে। ছবির বিটম্যাপ ডেটা অ্যারের প্রতিটি বাইট একটি একক পিক্সেল প্রতিনিধিত্ব করে। সেই বাইটের মান হল bmciColors দ্বারা উপস্থাপিত 256 এন্ট্রি থেকে ব্যবহৃত রঙ প্যালেট এন্ট্রির সংখ্যা।
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. কিন্তু আপনি দেখতে পাচ্ছেন, এটির প্রয়োজন নেই, যেহেতু পিক্সেল ডেটা নিজেই রঙের তথ্য ধারণ করে।
|32 বিট ফরম্যাট|32 বিট ইমেজ সর্বাধিক 2^24 রং আছে (biBitCount == 24)।

## তথ্যসূত্র ##
  * [ডিভাইস-ইনডিপেনডেন্ট বিটম্যাপস - মাইক্রোসফট দ্বারা](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

