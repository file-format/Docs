{
  "date" : "2021-06-24",
  "keywords" : [ "PART", "partial", "extension", "file", "format", "web", "downloaded" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PART - আংশিক ডাউনলোড করা ফাইল",
  "description":"PART ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা PART ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## একটি PART ফাইল কি? ##

একটি অংশ ফাইল বা .পার্ট এক্সটেনশন একটি আংশিক ডাউনলোড করা ফাইল। এটি ব্যবহার করা হয় যখন ডাউনলোডগুলি চলছে বা কোনও সমস্যার কারণে বাধাগ্রস্ত হয়েছে, ডাউনলোড ম্যানেজারকে যখনই সম্ভব ডাউনলোড পুনরায় শুরু করার সুযোগ দেয়।
এর মানে হল যে ব্রাউজার, যেমন ফায়ারফক্স বা ফাইল ট্রান্সফার প্রোগ্রাম যেমন eMule, eMule plus, FlashGet, ইত্যাদি ফাইলের একটি অংশ সঞ্চয় করে, যাকে বলা হয় Part file, যখন আপনার ডিভাইসে ডাউনলোড হচ্ছে। এই অংশ ফাইলটি আপনাকে দেখাবে যে ডাউনলোডটি চলছে কিনা বা সম্পূর্ণ হওয়ার আগে বাধাগ্রস্ত হয়েছে। শুধু তাই নয়, PART ফাইলটি ডাউনলোড সম্পূর্ণ না হওয়া পর্যন্ত সমস্ত ডেটা সঞ্চয় করে যার কারণে আপনি যদি আবার ডাউনলোড শুরু করতে চান তবে সেগুলির মধ্যে কিছু আবার শুরু করা যেতে পারে।

## অংশ ফাইল বিন্যাস ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
