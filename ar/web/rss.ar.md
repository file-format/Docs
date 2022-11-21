{
  "date" : "2021-06-24",
  "keywords" :["RSS" , "جزئية" , "امتداد" , "ملف" , "تنسيق" , "ويب" , "Really Simple Syndication" , "برنامج Userland"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Really Simple Syndication" ,
  "description":"تعرف على تنسيق ملف RSS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RSS وفتحها." ,
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-24"
}

## ما هو ملف RSS؟ ##

يُعرف الملف بالملحق .rss باسم Really Simple Syndication. RSS هو نوع ملف يسهل قراءته بواسطة الكمبيوتر ، ملف XML. يتم تحديث ملفات XML هذه تلقائيًا بأي تغييرات في البيانات أو تحديثات موقع ويب أو صفحة ويب. يتم استخراج المعلومات المحدثة إلى جانب البيانات الوصفية (اسم المؤلف ، واسم الناشر ، وتاريخ النشر ، وما إلى ذلك) ومحتوى الويب الآخر لموقع الويب بواسطة ملفات RSS الخاصة بالمستخدم ويتم تقديمها بتنسيق سهل القراءة. أفضل ميزة لملفات RSS هذه هي أنها تعمل في الوقت الفعلي ، ويتم عرض التحديثات والأخبار والنشر ، وهو الأحدث ، في أعلى الملف. باستخدام ملف RSS ، يمكنك بسهولة إنشاء ملف يحتوي على آخر التحديثات لأي موضوع تهتم به ، عن طريق سحب المحتوى ذي الصلة من الويب وقراءته باستخدام ملف RSS.

## نبذة تاريخية ##

في جوهره ، تم إنشاء ملف RSS لأول مرة بواسطة Netscape ، حيث اخترعوا الإصدار الأول من ملف RSS ولكنهم بعد ذلك أسقطوا الفكرة ، ولم يستمروا في الإصدارات الأحدث. ثم كان ** Userland Software ** هو الذي عمل على تنسيق ملف RSS واستمر في ابتكاره بإصدار أحدث ، وهذه هي الطريقة التي ظهرت بها RSS v2 في السوق. ومع ذلك ، يمكن ربط اختراع RSS مرة أخرى بإطار عمل وصف الموارد ، بواسطة Ramanathan V في عام 1997. إن طريقة عمل الملفين متشابهة جدًا ومن الآمن افتراض أن مفهوم RSS قد تم تشكيله بناءً على أعمال RDF ، قارئ ملف تم استخدامه لجمع البيانات الوصفية.

## مواصفات تكنيكال ##

ملف RSS هو نوع من ملفات XML ويجب أن تتبع جميع ملفات RSS معايير XML 1.0. هناك إصدارات مختلفة من ملفات RSS المختلفة ، مثل 0.91 و 0.92 و 2.0 وغيرها. يتوافق ملف كل إصدار مع المواصفات والمعايير الخاصة بذلك الإصدار المحدد.

## مثال RSS ##

فيما يلي مثال مبسط عن خدمة RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## المرجعي ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
