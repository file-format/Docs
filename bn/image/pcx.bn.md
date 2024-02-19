{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PCX ফাইল ফরম্যাট - পেইন্টব্রাশ বিটম্যাপ ইমেজ ফাইল",
  "description": "PCX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি PCX ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pcx-bn"
    }
  },
  "lastmod": "2022-03-16"
}

## একটি PCX ফাইল কি?

পিসিএক্স ফাইল, পিকচার এক্সচেঞ্জ ফাইল, একটি রাস্টার ইমেজ ফাইল ফরম্যাট যা পিসি পেইন্টব্রাশ অ্যাপ্লিকেশনের জন্য নেটিভ ফাইল ফরম্যাট হিসাবে ব্যবহৃত হয়েছিল। এটি DOS এবং Windows প্ল্যাটফর্মের জন্য ZSoft Corporation, USA দ্বারা তৈরি করা হয়েছিল এবং [BMP](/image/bmp/), [JPEG](/image/jpeg/), এবং [PNG](/image/png/) ফাইল ফর্ম্যাটের আগমনের আগে এটিকে প্রধান ইমেজিং ফাইল ফর্ম্যাট হিসাবে গৃহীত হয়েছিল৷ PCX ফাইলগুলি আকারে ছোট কারণ সেগুলি RLE এনকোডিং ব্যবহার করে সংকুচিত হয়। এটি বহু-পৃষ্ঠা [DCX](/image/dcx/) ফাইলে ব্যবহৃত হয় যা প্রাথমিকভাবে ডিজিটাল ফ্যাক্স ফাইল তৈরি করতে ব্যবহৃত হয়।

## PCX ফাইল ফরম্যাট

PCX ফাইল বাইনারি ফাইল ফরম্যাটে ডিস্কে সংরক্ষিত হয়। অভ্যন্তরীণ ফাইল বিন্যাস কাঠামো সামান্য এন্ডিয়ান বাইট ক্রম অনুসরণ করে এবং নিম্নলিখিত তিনটি বিভাগ রয়েছে:

**`PCX হেডার`** - একটি PCX হেডার 128 বাইট দীর্ঘ। এটিতে একটি শনাক্তকারী, একটি সংস্করণ নম্বর, চিত্রের মাত্রা, 16টি প্যালেট রঙ, নম্বর রঙের প্লেন এবং প্রতিটি প্লেনের বিট গভীরতা এবং কম্প্রেশন পদ্ধতির জন্য একটি মান রয়েছে।

গ্রাফিক্স ফাইল ফরম্যাটের এনসাইক্লোপিডিয়া (২য় সংস্করণ) থেকে রেফারেন্স সহ PCX হেডার নীচে দেখানো হয়েছে।
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`ইমেজ ডেটা`** - পিসিএক্স ইমেজ ডেটা হেডারের ঠিক পরে অনুসরণ করে। হেডারে ফিল্ড সেটিং এর উপর নির্ভর করে ইমেজ ডেটা সংকুচিত হতে পারে। PCX ফাইলে ডেটার স্টোরেজ নির্দিষ্ট রঙের প্লেনের সংখ্যার উপর নির্ভর করে। ইমেজ ডেটা সারিতে সংগঠিত হয়। একাধিক প্লেনের ক্ষেত্রে, এগুলি লাল, সবুজ এবং নীল ডেটার ক্রমিক বিন্যাসের মধ্যে সারির মধ্যে সমতল দ্বারা সংরক্ষণ করা হয়। এই প্যাটার্ন সমতল প্রতিটি লাইন জন্য পুনরাবৃত্তি হয়.

## তথ্যসূত্র

* [PCX - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/PCX)


