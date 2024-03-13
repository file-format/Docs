{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ faylı - EAZ faylı nədir və onu necə açmaq olar?",
  "description":"EAZ fayl formatı və EAZ fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-azz"
}
},
  "lastmod" : "2023-12-23"
}

## EAZ faylı nədir?

EAZ faylı ArcGIS Explorer tərəfindən istifadə edilən əlavə fayldır, xəritənin kəşfiyyatı, vizuallaşdırılması və paylaşılması üçün ESRI tərəfindən hazırlanmış pulsuz proqramdır. O, [XML file](/web/xml/), tərtib edilmiş kodu və əlavə üçün lazım olan dəstəkləyici faylları ehtiva edən sıxılmış fayl arxivindən ibarətdir. Bu fayllar yeni düymələr, dok pəncərələr və digər uzantıları daxil etməklə proqram təminatının əsas funksionallığını genişləndirmək üçün istifadə olunur.

## EAZ Fayl Format - Ətraflı Məlumat

EAZ faylları ArcGIS Explorer-də xüsusi funksiyalar yaratmaq üçün nəzərdə tutulmuş inkişaf dəsti olan ArcGIS Explorer SDK-dan istifadə etməklə yaradılır. Bu fayllar məzmunlarını səmərəli şəkildə paketləmək üçün [ZIP](/compression/zip/) sıxılmadan istifadə edir. Arxivin əsas hissəsində **Addins.xml** faylı kök kataloqda yerləşir və EAZ faylına daxil edilmiş müxtəlif fərdiləşdirmələri təsvir edən və təfərrüatlandıran mühüm komponent kimi xidmət edir.

Addins.xml faylı EAZ faylının ArcGIS Explorer-ə təqdim etdiyi xüsusi təkmilləşdirmələr, modifikasiyalar və genişləndirmələr haqqında anlayışlar təklif edən yol xəritəsi rolunu oynayır. Bu hərtərəfli struktur vasitəsilə tərtibatçılar ArcGIS Explorer tətbiqinin ümumi funksionallığını və istifadəçi təcrübəsini təkmilləşdirərək yeni funksiyaları, düymələri və dockable pəncərələri əhatə edə və problemsiz şəkildə birləşdirə bilərlər.

## İstinadlar

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
