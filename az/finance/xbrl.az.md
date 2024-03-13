{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - Biznes və Maliyyə Hesabatı Fayl Formatı",
  "description":"XBRL faylları yarada və aça bilən XBRL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-az",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## XBRL faylı nədir?

.xbrl (Genişləndirilə bilən Biznes Hesabat Dili) genişləndirilməsi olan fayl biznes məlumatlarının mübadiləsi üçün sərbəst mövcud və qlobal çərçivədir. İndi o, köhnə kağız əsaslı hesabatları daha faydalı və dəqiq rəqəmsal qeydlərlə əvəz edən standart formatlardan biri kimi geniş istifadə olunur. XBRL fayllarından istifadə etməklə mübadilə edilən məlumatlara kitablar, maliyyə təfərrüatları və balans hesabatları daxildir. Bu, bütün növ biznes məlumatlarının hazırlanmasından təhlil mərhələsinə qədər məlumatların emalına imkan verən məlumat etiketlərini dəstəkləyir. XBRL faylları Rivet Software Dragon View XBRL Viewer kimi proqram təminatı və [Aspose.Finance](https://products.aspose.com/finance/) kimi API-lərdən istifadə etməklə açıla bilər.

## XBRL fayl formatı

XBRL qlobal miqyasda geniş istifadə olunan rəqəmsal biznes hesabatları üçün açıq beynəlxalq standartdır. Bu, hesabatların çeşidlənməsi və təhlili üçün məlumatları formalaşdırmaq üçün biznes məlumatlarının hər bir elementini təsvir etmək üçün teqlər kimi tanınan XBRL elementlərindən istifadə edən [XML](/web/xml/) əsaslı dildir. XBRL fayl formatının spesifikasiyaları hazırda istifadəçilər üçün əlçatan olan [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) ilə XBRL International, Inc tərəfindən hazırlanmış və nəşr edilmişdir.

### XBRL Sənəd Strukturu

[XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) haqqında tam məlumat proqramçılar tərəfindən bu fayl formatında işləmək üçün proqramlar yazmaq üçün istinad edilə bilər. XBRL bir XBRL nümunəsindən və taksonomiyalar toplusundan ibarətdir.

**`XBRL Nümunəsi`** - XBRL nümunəsi ilə başlayır<xbrl> kök elementi. Böyük XML sənədində birdən çox XBRL nümunəsi ola bilər.

**`XBRL Taksonomiyası`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) XML sxem strukturları və birbaşa istinad edilən xarici keçid elementləri dəsti kimi müəyyən edilir. Linkbase istinadlarını göstərən genişlənə bilən taksonomiya sxemi aşağıdakı kimidir.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## İstinadlar ##

* [XBRL - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/XBRL)

* [Genişləndirilə bilən Biznes Hesabat Dili (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+düzəldi- səhv-2013-02-20.html)


