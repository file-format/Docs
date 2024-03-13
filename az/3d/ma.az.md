{
  "date": "2019-10-11",
  "keywords": [
"ma",
"ma faylı",
"ma fayl formatı",
"fayl formatı",
"3d",
"ma faylı yükləmək",
".ma faylı",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "MA fayl formatı və MA fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "MA fayl formatı",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-aza"
}
},
  "lastmod": "2021-06-04"
}

## MA faylı nədir?

.ma uzantılı fayl Autodesk Maya proqramı ilə yaradılmış 3D layihə faylıdır. O, fayl haqqında məlumatı təyin etmək üçün mətn əmrlərinin böyük siyahısını ehtiva edir. **.ma faylı** faylın zədələnməsi halında əmrlərlə bağlı hər hansı problemi həll etmək üçün istənilən mətn redaktorunda açıla və redaktə edilə bilər. Bu fayllar həndəsə, işıqlandırma, animasiya və göstərmə kimi 3D Səhnə məlumatını müəyyən etmək üçün məlumatları ehtiva edir.

## MA fayl formatı

MA faylları diskdə ikili fayl formatında saxlanılan MB fayllarından fərqli olaraq ASCII mətn formatında diskdə saxlanılır. MA fayl formatı üçün ətraflı arayış [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)-də mövcuddur və onu tərtibatçının arayışı üçün istinad etmək olar.

### MA Fayl Başlığı

MA faylının başlığı faylın yaradılması məlumatını və dəyişdirilmiş tarixi verən şərhlər bölməsi ilə başlayır. Maya faylı oxucuları bu bloka məhəl qoymurlar, çünki o, yalnız məlumat məqsədi ilə istifadə olunur. Başlıq //Maya kimi ilk altı simvolla başlamalıdır.

ASCII fayl başlığı aşağıdakı kimi görünür.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Fayl İstinadları

.ma faylının fayl istinadları bölməsində bu faylda istinad edilən bütün digər Maya faylları haqqında məlumat var. İstinad edilən hər bir fayl eyni faylda olan bir fayl əmrindən istifadə etməklə oxuna bilər. İstinad üçün istifadə edildikdə fayl əmrinin sintaksisi belədir:

```
file -r -rpr prefixString fileName;
```
və ya

```
file -r -ns nameSpace fileName
```
Burada misal sətirdir.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Bu nümunə göstərir ki, `solar` faylında olan günəş obyekti bu faylda solar_sun adından istifadə etməklə əldə edilə bilər.

### Tələblər

.ma faylının Tələblər bölməsi bir sıra tələb olunan əmrlərdən ibarətdir və faylları oxumaq üçün tələb olunan versiya və plagin məlumatı kimi may ayı məlumatlarını bildirir. Tələblər bölməsinin nümunəsi aşağıdakı kimidir.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Növbəti bölmə tələbləri müəyyən edir. Bu, bir sıra tələb olunan əmrlərdən ibarətdir. Faylın bu bölməsi Maya faylı düzgün yükləmək üçün hansı proqram təminatının lazım olduğunu bildirir. Konkret olaraq, Maya-nın hansı versiyası və hansı plaginlər.

## MA faylı yükləyin
3D modelin MA faylını tapmaq və yükləmək bir qədər çətindir. Buna görə, nümunə MA faylını buradan yükləyə bilərsiniz:

- [Sample.ma](../sample.ma)


## İstinadlar

* [Maya ASCII Fayllarının Təşkili - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


