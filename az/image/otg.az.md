{
  "date": "2020-01-10",
  "keywords": [
"otg faylı",
"otg fayl formatı",
"otg faylı nədir",
"fayl",
"otg misal",
"otg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG - OpenDocument Çizim Şablon Fayl Formatıdır",
  "description": "OTG fayl formatı və OTG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-azg"
}
},
  "lastmod": "2020-01-10"
}

## OTG faylı nədir?

OTG faylı OASIS Office Applications 1.0 spesifikasiyasına uyğun olaraq OpenDocument standartından istifadə etməklə yaradılmış rəsm şablonudur. Bu, faylın məzmununu daha da təkmilləşdirmək üçün istifadə edilə bilən vektor təsviri üçün rəsm elementlərinin standart təşkilini təmsil edir. OTF faylları sənədin məzmununu təmsil etmək üçün XML formatına əsaslanan hər hansı digər OpenDocument format əsaslı fayllar kimidir. OTF faylları istənilən mətndə və ya standart XML redaktorunda açaraq baxıla bilər.

## OTG Fayl Formatının Xüsusiyyətləri ##

OTG fayl formatı yaxşı qurulmuş sxemə malik OpenDocument XML formatına əsaslanır. OpenDocument formatının hər bir komponentinin strukturu əlaqəli atributlara malik elementlə təmsil olunur və mətn sənədi, elektron cədvəl və ya rəsm faylı kimi bütün sənəd növləri üçün ümumidir. Rəsm şablonu olan OTG, aşağıdakıları ehtiva edən Qrafik Məzmun spesifikasiyalarından geniş şəkildə istifadə edir:

  * Qrafik Tətbiqlər üçün Təkmilləşdirilmiş Səhifə Xüsusiyyətləri
  * Formaların çəkilməsi
  * Çərçivələr
  * 3D Fiqurlar
  * Xüsusi Forma
  * Təqdimat formaları
  * Təqdimat animasiyaları
  * SMIL təqdimat animasiyaları
  * Təqdimat tədbirləri
  * Hazırkı Mətn Sahələri
  * Təqdimat sənədinin məzmunu

### Qrafik Tətbiqlər üçün Təkmilləşdirilmiş Səhifə Xüsusiyyətləri ###
#### Təqdimat Ustası ####

Handout Master elementi bu cür səhifələrin çapını dəstəkləyən proqramlar üçün paylama səhifələrini avtomatik yaratmaq üçün şablondur.
` ilə əlaqələndirilə bilən atributlar<style:handout-master> ` elementi bunlardır:

|Layout|Atribut|Təsvir
---|---|---|
|Təqdimat Səhifəsinin Düzəlişi|təqdimat:presentation-page-layout-name|Bağlantılar `<style:presentation-page-layout> ` atribut
|Səhifənin Düzəlişi|`stil:səhifə-layout-name` | Təqdim olunan əsas səhifənin ölçülərini, haşiyəsini və oriyentasiyasını ehtiva edən səhifə tərtibatını müəyyən edir.
|Səhifə Stili|`draw:style-name`|Çizgi səhifə stili təyin etməklə paylanma materialının əsas səhifəsinə əlavə format atributları təyin edir.|
|Başlıq Bəyannaməsi| `təqdimat:use-header-name`| Təqdim olunan materialın əsas səhifəsində göstərilən bütün başlıq sahələri üçün istifadə olunan başlıq sahəsi bəyannaməsinin adını müəyyən edir.
|Alt-bilgi Bəyannaməsi| presentation:use-footer-name|Təhsil materialının əsas səhifəsində göstərilən bütün altbilgi sahələri üçün istifadə olunan altbilgi sahəsi bəyannaməsinin adını müəyyən edir.
|Tarix və Saat Bəyannaməsi|use-date-time-name|Təqdimat materialının əsas səhifəsində göstərilən bütün tarix-vaxt sahələri üçün istifadə olunan tarix-vaxt sahəsi bəyannaməsinin adını müəyyən edir.

### Formaları Çəkmək ###
OpenDocument formatı istənilən sənəd növü tərəfindən istifadə oluna bilən bir neçə rəsm şəklini dəstəkləyir.

|Forma|Əlaqəli Atributlar| elementləri
---|---|---|
Düzbucaqlı - `<draw:rect> `|Mövqe, Ölçü, Üslub, Qat, Z-indeks, ID, Başlıq ID, Mətn ankeri, cədvəl fonu, son mövqe, Dairəvi künclər|Başlıq, Uzun Təsvir, Tədbir Dinləyiciləri, Yapışqan Nöqtələr, Mətn
Xətt `<draw:line> `|Üslub, Layer, Z-indeks, ID, Başlıq ID və Çevrilmə, Mətn ankeri, cədvəl fonu, çəkiliş son mövqeyi, Başlanğıc nöqtəsi, Son Nöqtə|Başlıq, Uzun Təsvir, Tədbir Dinləyiciləri, Yapışqan Nöqtələr, Mətn
Polyline `<draw:polyline> `| Mövqe, Ölçü, Görünüş qutusu, Üslub, Qat, Z-indeksi, ID, Başlıq ID və Çevrilmə, Mətn ankeri, cədvəl fonu, son mövqe, Xallar| Başlıq, Uzun Təsvir, Hadisə Dinləyiciləri, Yapışqan Nöqtələr, Mətn
Poliqon `<draw:polygon> `|Mövqe, Ölçü, Görünüş qutusu, Üslub, Layer, Z-indeks, ID, Başlıq ID və Çevrilmə, Mətn lövbəri, cədvəl fonu, çəkiliş son mövqeyi, Xallar|Başlıq, Uzun Təsvir, Tədbir dinləyiciləri, Yapışqan nöqtələri, Mətn
|Normal Poliqon `<draw:regular-polygon> `|Mövqe, Ölçü, Üslub, Qat, Z-indeks, ID, Başlıq ID və Çevrilmə, Mətn lövbəri, cədvəl fonu, çəkiliş son mövqeyi, Konkav, Künclər, Kəskinlik|Başlıq, Uzun Təsvir, Tədbir dinləyiciləri, Yapışqan nöqtələri, Mətn
|Paht `<draw:path> `|Mövqe, Ölçü, Görünüş qutusu, Üslub, Layer, Z-indeks, ID, Başlıq ID və Transformasiya, Mətn ankeri, cədvəl fonu, son mövqe, Yol datası| Başlıq, Uzun Təsvir, Hadisə Dinləyiciləri, Yapışqan Nöqtələr, Mətn

### Çərçivələr ###
Çərçivə sənədində mətn qutuları, şəkillər və ya obyektlər olan düzbucaqlı bir konteynerdir. Çərçivələr konturlar, şəkil xəritələri və hiperlinklər kimi əlavə funksiyaları dəstəkləyir. Çərçivə həm obyekti, həm də təsviri ehtiva edə bilər, beləliklə, bir obyektin bir neçə renderasiyasına imkan verir. Tətbiqlər ən yaxşı dəstəyə əsaslanaraq müvafiq elementi təqdim edir.

Çərçivələrdə ola bilər:
  * Mətn qutuları
  * Obyektlər ya OpenDocument formatında, ya da obyektə məxsus ikili formatda təmsil olunur
  * Şəkillər
  * Appletlər
  * Pluginlər
  * Üzən çərçivələr

Aşağıda göstərildiyi kimi sənəddə çərçivə var.

```
<define name=draw-frame>
<element name=draw:frame>
<ref name=common-draw-shape-with-text-and-styles-attlist/>
<ref name=common-draw-position-attlist/>
<ref name=common-draw-rel-size-attlist/>
<ref name=common-draw-caption-id-attlist/>
<ref name=presentation-shape-attlist/>
<ref name=draw-frame-attlist/>
<zeroOrMore>
<choice>
<ref name=draw-text-box/>
<ref name=draw-image/>
<ref name=draw-object/>
<ref name=draw-object-ole/>
<ref name=draw-applet/>
<ref name=draw-floating-frame/><ref name=draw-plugin/>
</choice>
</zeroOrMore>
<optional>
<ref name=office-event-listeners/>
</optional>
<zeroOrMore>
<ref name=draw-glue-point/>
</zeroOrMore>
<optional>
<ref name=draw-image-map/>
</optional>
<optional>
<ref name=svg-title/>
</optional>
<optional>
<ref name=svg-desc/>
</optional>
<optional>
<choice>
<ref name=draw-contour-polygon/><ref name=draw-contour-path/>
</choice>
</optional>
</element>
</define>
```

## İstinadlar ##
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


