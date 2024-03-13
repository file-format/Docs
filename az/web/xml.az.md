{
  "date": "2019-10-11",
  "keywords": [
"xml",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"genişləndirilə bilən işarələmə dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XML fayl formatı",
  "description": "XML faylları yarada və aça bilən XML fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-azl"
}
},
  "lastmod": "2019-09-10"
}

## XML faylı nədir?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML fayl formatı

XML fayl formatı HTML və XML sənədləri üçün proqramlaşdırma API olan XML Sənəd Obyekt Modelinə (DOM) əsaslanır. XML DOM XML sənəd elementlərinə daxil olmaq və onları idarə etmək üçün standart metodu müəyyən edir. DOM ağacı vasitəsilə bütün elementlərə daxil olmaq üçün istifadə edilə bilən XML sənədinin ağac strukturu görünüşünü yaradır. Mövcud elementlər dəyişdirilə/silə, həmçinin XML ağacında yeni elementlər yaradıla bilər. XML sənədinin hər bir elementi qovşaq adlanır. XML DOM aşağıdakı şəkildə göstərildiyi kimidir.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### XML-ə universal yanaşma

XML-in gücü məlumatların daşınmasını və platforma dəyişikliklərini sadələşdirərək, onu şəbəkə üzərindən məlumat kommunikasiyası üçün universal dilə çevirir. Bu, həm də məlumatları düz mətn formatında saxlamaqla uyğun olmayan sistemlər arasında məlumat mübadiləsini təmin edir. HTML internet üzərindən məlumat təqdim etmək üçün, XML isə məlumat mübadiləsi üçündür. XML daxilində istifadə olunan işarələmə etiket cütləri proqramların oxunması zamanı istifadə ediləcək strukturun əsas elementlərini müəyyənləşdirir.

## XML nümunəsi

Aşağıda CD kataloqunun sadələşdirilmiş nümunəsi verilmişdir, burada hər bir qeyddə CD-lər haqqında rəssam, ölkə, şirkət, qiymət və istehsal ili kimi məlumatlar var.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## İstinadlar

* [XML - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/XML)


