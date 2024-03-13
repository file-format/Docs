{
  "date": "2021-01-21",
  "keywords": [
"ai faylı",
"ai fayl formatı",
"ai faylı nədir",
"fayl",
"ai misal",
"ai fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI - Adobe Illustrator Artwork File",
  "description": "AI fayl formatı və AI faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-azi"
}
},
  "lastmod": "2021-01-21"
}

## AI faylı nədir?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI fayl formatı

AI Adobe Illustrator-un xüsusi fayl formatıdır və EPS uyğun faylları saxlamaq üçün PGF-ə bənzər ikili yol yanaşmasından istifadə edir. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) bu fayl formatının daxili təfərrüatları üçün ətraflı tərtibatçı arayışı təqdim edir. Adobe Illustrator tərəfindən yaradılan bütün sənədlər (fayllar) PostScript dil sənədləridir və Sənədin Strukturlaşdırılması Konvensiyalarına uyğun gələn iki əsas hissədən ibarətdir: proloq və skript.

### Proloq

Proloq bölməsi faylın təfsiri üçün tələb olunan məlumatları əhatə edir. Nümunə olaraq, səhifədəki bütün işarələri ehtiva edən məhdudlaşdırıcı qutu ola bilər. O, həmçinin şriftlər və prosedur tərifləri kimi resurslar məlumatını ehtiva edir. Bu resurslar məntiqi olaraq procsetlər adlanan dəstlərə qruplaşdırılıb və onların prosedurlarını işə salmaq və dayandırmaq üçün açıq üsulları ehtiva edir.

### Skript

Səhifədəki qrafik elementlər skriptlə təsvir olunur. Skriptdə operandlar və verilənlərlə birlikdə proloqdakı operatorlara və prosedurlara istinadlar var. Skriptin üç məntiqi bölməsinə aşağıdakılar daxildir:

 * Quraşdırma ardıcıllığı - proloqda müəyyən edilmiş resursları işə salır və aktivləşdirir
 * Təsviri operatorların ardıcıllığı
 * Resursları deaktiv edən treyler

Skriptdəki operatorlar proloqda procsetlər tərəfindən müəyyən edilmiş dildə yazılmış qrafik elementlərin ardıcıllığıdır. Bu ardıcıllıqlar məlumat elementlərinin kolleksiyalarından, qrafik atribut təriflərindən və prosedurlarda müəyyən edilmiş prosedurlara çağırışlardan ibarətdir.

### Obyekt Teqləri

Obyekt teqləri Adobe Illustrator incəsənət obyektinə fərdi məlumat əlavə etmək üçün istifadə olunur. Teqlər aşağıdakılardan ibarətdir:

 * Etiket identifikatoru
 * Etiket növü
 * Data

## İstinadlar
* [Adobe Illustrator Fayl Formatının Xüsusiyyətləri](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [PaintShopPro tərəfindən AI Fayl Formatı](https://www.paintshoppro.com/en/pages/ai-file/)


