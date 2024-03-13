{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"açıq"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL - ZK İstifadəçi İnterfeysi Faylı",
  "description": "ZUL faylları yarada və aça bilən ZUL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-azl"
}
},
  "lastmod": "2021-05-24"
}

## ZUL faylı nədir?

.zul uzantılı fayl İstifadəçi İnterfeysi İşarələmə Dili (ZUML) ilə yaradılmış veb fayldır və istifadəçi interfeysi elementləri üçün tərifləri ehtiva edir. Ajax və Java sinifləri server tərəfi faylları hazırlamaq üçün [XML](/web/xml/) əsaslı ZUML istifadəsini dəstəkləyir. ZUL fayl formatı JavaScript və ya AJAX biliyi olmadan veb və mobil proqramlar yaratmağa imkan verən UI çərçivəsi olan ZK tərəfindən hazırlanmışdır.

## ZUL fayl formatı

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL Nümunəsi

Aşağıdakı ZUML kodu nümunəsində birinci sətir səhifə başlığını təyin edir, ikinci sətir başlıq və haşiyə ilə kök komponenti, üçüncü sətir isə etiket və hadisə dinləyicisi olan düymə yaradır.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL sxemini https://www.zkoss.org/2005/zul/zul.xsd saytından yükləmək olar.
## İstinadlar

* [ZUL - By ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [ZUL Şeması](https://www.zkoss.org/2005/zul/zul.xsd)


