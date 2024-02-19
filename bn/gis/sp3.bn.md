{
  "date": "2021-08-24",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "SP3 - NGS SP3 ফাইল",
  "description": "SP3 ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা SP3 ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "SP3",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sp3-bn"
    }
  },
  "lastmod": "2021-09-29"
}

## একটি SP3 ফাইল কি?

A file with .sp3 extension is a National Geodetic Survey (NGS) orbital format to store orbital information. This is an extension to NGS's SP1 and SP2 formats, and includes the satellite clock correction information that is computed simultaneously with the orbits. It is primarily based on position and clock, and does not include velocities. The format was proposed in Remondi, 1989 and was adopted in 1991. স্যাটেলাইট ঘড়ি সংশোধন তথ্য ছাড়াও, এতে কক্ষপথের নির্ভুলতা সূচক, মন্তব্য লাইন, জিপিএস সপ্তাহ এবং প্রথম যুগের সাথে যুক্ত সপ্তাহের সেকেন্ডের মতো তথ্য অন্তর্ভুক্ত রয়েছে। SP3 ফাইল ওলফ্রাম রিসার্চ ম্যাথমেটিকা দিয়ে খোলা যেতে পারে।

## SP3 ফাইল ফরম্যাট - আরও তথ্য

SP3 ফাইলগুলি ASCII ফাইল ফরম্যাটে ডিস্কে সংরক্ষিত হয় এবং এর বিষয়বস্তু দেখার জন্য যেকোনো পাঠ্য সম্পাদকে খোলা যেতে পারে। একটি SP3 ফাইলের গঠন নিচের চিত্র থেকে দেখা যায়।

{{< figure src="../sp3-file-format.png" title="" >}}

## তথ্যসূত্র

* [দ্য এক্সটেন্ডেড স্ট্যান্ডার্ড প্রোডাক্ট 3 অরবিট ফরম্যাট (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20আরও%20নমনীয়%20হেডার%20স্ট্রাকচার)

* [জাতীয় জিওডেটিক সার্ভে স্ট্যান্ডার্ড জিপিএস অরবিট ফরম্যাটগুলি প্রসারিত করা](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)


