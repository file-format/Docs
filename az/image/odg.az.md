{
  "date": "2019-10-11",
  "keywords": [
"odg faylı",
"odg fayl formatı",
"odg faylı nədir",
"fayl",
"odg nümunəsi",
"odg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODG fayl formatı",
  "description": "ODG fayl formatı və ODG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-azg"
}
},
  "lastmod": "2019-09-10"
}

## ODG faylı nədir?

ODG fayl formatı rəsm elementlərini vektor şəkli kimi saxlamaq üçün Apache OpenOffice-in Draw proqramı tərəfindən istifadə olunur. O, Struktur Məlumat Standartlarının Təkmilləşdirilməsi (OASIS) tərəfindən qeyd olunan XML əsaslı fayl formatı spesifikasiyalarına uyğundur. ODG nöqtələr, xətlər və əyrilərdən istifadə edərək vektor şəkilləri kimi təsvirləri təmsil edir. OpenOffice ilə yanaşı, LibreOffice və digər proqramlar da ODG fayl formatı ilə işləmək üçün dəstək verir. OpenOffice tərəfindən dəstəklənən digər formatlara, məsələn, [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) və [ODS](/spreadsheet/ods/) daxildir.


## ODG Fayl Formatının Xüsusiyyətləri

ODG fayl formatı yaxşı müəyyən edilmiş sxemə malik strukturlaşdırılmış XML sənəd formatı olan OpenDocument formatına əsaslanır.
OpenDocument formatının hər bir struktur komponenti əlaqəli atributları olan elementlə təmsil olunur. XML əsaslı struktur mətn sənədi, elektron cədvəl və ya rəsm faylı kimi bütün sənəd növləri üçün ümumidir. Sənəddə müxtəlif üslublar ola bilər. OpenDocument fayl strukturu aşağıdakı elementlərdən ibarətdir.
  * Sənəd Kökü
  * Sənəd MetaData
  * Bədən Elementi və Sənəd növləri
  * Tətbiq Parametrləri
  * Skriptlər
  * Şrift Üz Bəyanatları
  * Üslublar
  * Səhifə üslubları və düzənləri

##  Sənəd Kökləri ##

Sənədin kök elementi bütün sənədi ehtiva edir və OpenDocument formatında faylın əsas elementidir. Sənədin kök elementlərinin eyni növləri mətn, sənədlər, cədvəllər və rəsm sənədləri kimi bütün növ sənədlərə şamil edilir.

### Kök Elementlər ###
Tək XML sənədi öz kök elementi ilə təmsil olunur. Beş fərqli dəstəklənən kök elementi aşağıdakı kimidir.

`<office:document> ` - SingleXML sənədində ofis sənədini tamamlayın.
`<office:document-content> ` - Sənəd məzmunu və məzmunda istifadə olunan avtomatik üslublar.
`<office:document-styles> ` - Sənədin məzmununda istifadə olunan üslublar və üslubların özlərində istifadə olunan avtomatik üslublar.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Pəncərə ölçüsü və ya printer məlumatı kimi proqrama xas parametrlər.

### ODG Sənədi MetaData ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Bədən Elementi və Sənəd Növləri ###
Sənədin əsas hissəsi sənəd növü elementindən istifadə edərək sənəddə olan məzmunun növünü göstərir. Bu sənəd növləri bunlardır:
  * mətn sənədləri
  * rəsm sənədləri
  * təqdimat sənədləri
  * elektron cədvəl sənədləri
  * diaqram sənədləri
  * şəkil sənədləri

### Tətbiq Parametrləri ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Sənəd parametrləri, məsələn, standart printer
  * Parametrlərə baxın, məsələn, böyütmə səviyyəsi

### Skriptlər ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Şrift Üz Bəyanatları ###

Şrift üz bəyannaməsində sənəd müəllifinin istifadə etdiyi şriftlər haqqında məlumat var. Bu məlumat bu şriftləri digər sistemlərdə tapmağa kömək edir.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Üslublar ###
Aşağıdakı üslublar OpenDocument formatı tərəfindən dəstəklənir.

`Ümumi Üslublar` - Belə üslubların XML təsvirlərinə üslublar deyilir
`Avtomatik Üslublar` - Sənədin istifadəçi interfeysi görünüşündə paraqraf kimi obyektə təyin edilən formatlaşdırma xassələrini ehtiva edir.
`Mater Styles` - formatlama məlumatını və üslub tətbiq edildikdə sənəd məzmunu ilə birlikdə göstərilən əlavə məzmunu ehtiva edən ümumi üslub. Usta üslubun nümunəsi əsas səhifələrdir.

## İstinadlar ##
  * [Ofis Proqramları üçün OASIS Açıq Sənəd Formatı](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

