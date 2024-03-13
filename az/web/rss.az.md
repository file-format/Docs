{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"qismən",
"uzadılması",
"fayl",
"format",
"veb",
"Həqiqətən Sadə Sindikasiya",
"İstifadəçi ölkə proqramı"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS - Həqiqətən Sadə Sindikasiya",
  "description": "RSS fayl formatı və RSS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-azs"
}
},
  "lastmod": "2021-06-24"
}

## RSS faylı nədir? ##

.rss uzantılı fayl Really Simple Syndication kimi tanınır. RSS kompüter tərəfindən asanlıqla və ya asanlıqla oxunan fayl növüdür, XML faylıdır. Bu XML faylları veb-saytın və ya veb-səhifənin məlumatlarında və ya yeniləmələrində hər hansı dəyişikliklə avtomatik olaraq yenilənir. Yenilənmiş məlumat metadata (müəllifin adı, naşirin adı, nəşr tarixi və s.) və veb-saytın digər veb məzmunu ilə birlikdə istifadəçinin RSS faylları tərəfindən çıxarılır və asan oxunan formatda təqdim olunur. Bu RSS fayllarının ən yaxşı xüsusiyyəti onun real vaxt rejimində işləməsidir və yeniləmələr, xəbərlər, nəşrlər, yəni ən son, faylın yuxarı hissəsində göstərilir. RSS faylından istifadə edərək, internetdən əlaqəli məzmunu götürərək və RSS faylından istifadə edərək oxumaqla maraqlandığınız hər hansı bir mövzunun ən son yeniləmələrini ehtiva edən faylı asanlıqla yarada bilərsiniz.

## Qısa tarix ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. İki faylın iş prinsipi olduqca oxşardır və güman etmək olar ki, RSS konsepsiyası metadata toplamaq üçün istifadə edilən fayl oxuyucusu olan RDF-nin işlərinə əsaslanaraq formalaşıb.

## Texniki Spesifikasiya ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Müxtəlif RSS fayllarının 0.91, 0.92, 2.0 kimi müxtəlif versiyaları var. Hər versiyanın faylı həmin xüsusi versiyanın spesifikasiyasına və standartlarına uyğundur. 

## RSS nümunəsi ##

Aşağıda RSS-in sadələşdirilmiş nümunəsi verilmişdir.

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
## İstinad ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
