{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portativ Sənəd Formatı (PDF) proqram, aparat və ƏS-dən asılı olmayaraq sənədlərin standart təqdimatıdır. PDF standartlarına PDF/A, PDF/E, PDF/UA, PDF/VT və PDF/X daxildir.",
  "title" : "PDF fayl formatı - PDF faylı nədir?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
"çəki : 01"
}
},
  "lastmod" : "2019-09-10"
}

Portativ Sənəd Format (PDF) Adobe tərəfindən 1990-cı illərdə yaradılmış sənəd növüdür. Bu fayl formatının məqsədi sənədlərin və digər istinad materiallarının tətbiqi proqram təminatından, aparat təminatından və əməliyyat sistemindən asılı olmayan formatda təqdim edilməsi üçün standart təqdim etmək idi. PDF fayl formatı mətn, şəkillər, hiperlinklər, forma sahələri, zəngin media, rəqəmsal imzalar, qoşmalar, metadata, geoməkan xüsusiyyətləri və mənbə sənədin bir hissəsi ola biləcək 3D obyektlər kimi məlumatları ehtiva etmək üçün tam imkanlara malikdir.

Əksər hallarda, mövcud sənədlər sıfırdan yeni PDF yaratmaq əvəzinə PDF-ə çevrilir. Lakin bu o demək deyil ki, PDF fayllarının yaradılması və ya manipulyasiyası üçün proqram təminatı yoxdur.

**(PDF fayl formatı haqqında nəsə paylaşmalısan? Nəticələrinizi [PDF File Format News](https://news.fileformat.com/t/PDF) bölməsində dərc edə bilərsiniz.)**

## PDF Fayl Format - Qısa Tarix

Taymlayn baxımından [PDF file format](https://products.fileformat.com/pdf/) ilə bağlı qrafiki qısaca nəzərdən keçirmək aşağıdakı kimidir:

**1993** - Adobe Systems PDF spesifikasiyalarını pulsuz təqdim etdi

**2008** - PDF 1 iyul 2008-ci ildə açıq standart olaraq buraxıldı və Beynəlxalq Standartlaşdırma Təşkilatı tərəfindən **ISO 32000-1:2008** kimi nəşr olundu.

**2008** - Adobe, PDF uyğun tətbiqləri hazırlamaq, istifadə etmək, satmaq və yaymaq üçün zəruri olan Adobe-yə məxsus bütün patentlər üçün ISO 32000-1 formatı üçün qonorarsız hüquqlar üzrə İctimai Patent Lisenziyasını nəşr etdi.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. ISO 32000-1-ə çevrilmiş PDF 1.7 bəzi qeyri-standart mülkiyyət texnologiyalarını, həmçinin Adobe XML Forms Architecture (XFA) və Acrobat üçün JavaScript genişləndirilməsini əhatə edir. 28 iyul 2017-ci ildə ISO 32000-2:2017 kimi tanınan PDF 2.0 standartlaşdırılmamış texnologiyaları ehtiva etməyən zaman nəşr olundu.

## PDF Fayl Formatının Xüsusiyyətləri

PDF faylı PDF spesifikasiyaları ilə müəyyən edilmiş sintaksis qaydalarına uyğun olaraq tokenlərə qruplaşdırıla bilən baytlar toplusudur. Bir və ya daha çox token daha yüksək səviyyəli sintaktik obyektlər, əsasən, PDF sənədinin qurulduğu əsas məlumat dəyərləri olan obyektlər yaratmaq üçün birləşdirilir.

### PDF fayllarının fayl strukturu

PDF faylının məzmunu fayl daxilində aşağıdakı ardıcıllıqla düzülür.

|Başlıq
|Bədən
| Çarpaz İstinad Cədvəli
|Treyler

#### PDF Fayl Başlığı ####

PDF versiyasından asılı olmayaraq, PDF faylı PDF üçün unikal identifikatoru və %PDF-1.x kimi format versiyasını ehtiva edən başlıq ilə başlayır, burada x 1-7 arasında dəyişir.

#### Fayl Gövdəsi ####

PDF faylının gövdəsi sənədin məzmununu təmsil edən dolayı obyektlərin ardıcıllığından ibarətdir. Obyektlər, yuxarıda təsvir edildiyi kimi, şriftlər, səhifələr və nümunə şəkillər kimi sənədin komponentlərini təmsil edir. PDF 1.5-dən başlayaraq gövdə həmçinin hər biri dolayı obyektlərin ardıcıllığını ehtiva edən obyekt axınlarını ehtiva edə bilər.

#### Çarpaz İstinad Cədvəli ####

Çarpaz istinad cədvəli fayl daxilindəki dolayı obyektlərə təsadüfi giriş imkanı verən məlumatları ehtiva edir ki, hər hansı xüsusi obyekti tapmaq üçün bütün faylın oxunmasına ehtiyac olmasın. Cədvəldə hər bir dolayı obyekt üçün faylın mətnində həmin obyektin bayt ofsetini göstərən bir sətirlik qeyd olmalıdır. (PDF 1.5-dən başlayaraq, çarpaz istinad məlumatlarının bir hissəsi və ya hamısı alternativ olaraq çarpaz istinad axınlarında ola bilər.

#### Fayl Treyleri ####

PDF faylının treyleri uyğun oxucuya çarpaz istinad cədvəlini və müəyyən xüsusi obyektləri tez tapmağa imkan verir. Uyğun olan oxucular PDF faylını sonundan oxumalıdırlar. Faylın son sətirində yalnız faylın sonu markeri, %%EOF olmalıdır. Əvvəlki iki sətir, hər sətirdə bir və ardıcıl olaraq, startxref açar sözünü və faylın əvvəlindən axırıncı çarpaz istinad bölməsindəki xref açar sözünün əvvəlinə qədər deşifrə olunmuş axındakı bayt ofsetini ehtiva etməlidir.

### PDF Obyektləri ###

PDF faylına aşağıdakı növlərdən olan bir neçə müxtəlif növ obyekt daxildir

* Boolean dəyərləri - şərti doğru və ya yalanı təmsil edir

* Nömrələr - Tam və Real dəyərlər

* Sətirlər - mötərizə içərisində simvolları ehtiva edir

* Adlar - irəli / simvol ilə başlayın, məsələn, /ASomewhatLongerName ASomewhatLongerName ilə nəticələnir

* Massivlər - PDF bir ölçülü massivləri dəstəkləyir. Daha yüksək ölçülü massivlər massivləri iç-içə elementlər kimi istifadə etməklə tikilə bilər

* Lüğətlər - obyektlərin açar-dəyər cütləri kimi toplanması. Sıfır giriş ola bilər.

* Axınlar - həm də qeyri-məhdud uzunluqda ola bilən baytların ardıcıllığını təmsil edir

* Null Object - null dəyəri təmsil edir


% işarəsi ilə təqdim edilən və 8 bit simvoldan ibarət olan şərhlər kimi başqa obyektlər də ola bilər.

### Dolayı Obyektlər ###

PDF faylındakı hər hansı obyekt dolayı obyekt kimi etiketlənə bilər. Dolayı obyektlərə digər obyektlərin ona istinad edə biləcəyi unikal obyekt identifikatoru verilir. Bunlara çarpaz istinad indeks cədvəlində saxlanılır və əsas gövdədən sonra gələn və faylın əvvəlindən hər dolayı obyektin bayt ofsetini verən xref açar sözü ilə qeyd olunur.

### Xətti və Qeyri-xətti PDF Planları ###

PDF tərtibatları hədəf tətbiqlərdən və digər amillərdən asılı olaraq Llnear və qeyri-xətti olaraq təsnif edilir.

Qeyri-xətti - Qeyri-xətti PDF faylları xətti PDF faylları ilə müqayisədə daha az disk sahəsi istifadə edir. Sənədin PDF səhifələri PDF faylı arasında səpələnmiş formada yerləşir və buna görə də qeyri-xətti fayllar xətti fayllarla müqayisədə daha yavaşdır.

Xətti PDF - Onlayn PDF izləyicilərini hədəf alan Xətti PDF faylları xətti şəkildə diskə yazılacaq şəkildə qurulur. Bu, bütün sənədin nümayişdən əvvəl yüklənməsi üçün brauzer plaginlərini tələb etmir.

### Obyektlərə Baxış ###

Qeyd edildiyi kimi, PDF orqanı yuxarıda qeyd olunan obyektlərin toplusudur. PDF əsasən if və loop əmrləri kimi proqramlaşdırma dillərinin idarəetmə xüsusiyyətləri olmadan PostScript-ə əsaslanır. Qrafik məzmun yaratmaq üçün Postscript kodu tərəfindən verilən əmrlər sənədin istinad etdiyi hər hansı fayl, qrafika və ya şriftlərə əlavə olaraq toplanır və işarələnir. Bütün bu məzmunlar bir faylda toplanır və nəticədə PostScript çıxışı yaranır.

#### Mətn ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Qrafik ####

PDF məzmun axınlarında istifadə olunan qrafik operatorları rastr çıxış cihazında çoxaldılmalı olan səhifələrin görünüşünü təsvir edir. Obyektlər həm printer, həm də displey proqramları üçün nəzərdə tutulub. Qrafik operatorlar altı əsas qrup təşkil edir:

* Qrafik dövlət operatorları digər qrafik operatorlarının icra etdiyi qlobal çərçivə olan qrafik dövlət adlanan məlumat strukturunu manipulyasiya edir. Qrafik vəziyyətə PDF məzmun axınında istifadə olunan istifadəçi məkanı koordinatlarını çıxış cihazının koordinatlarına uyğunlaşdıran cari transformasiya matrisi (CTM) daxildir. O, həmçinin cari rəngi, cari kəsmə yolunu və rəngləmə operatorlarının gizli operandları olan bir çox digər parametrləri ehtiva edir.

* Yol tikintisi operatorları formaları, xətt trayektoriyalarını və müxtəlif növ bölgələri müəyyən edən yolları təyin edir. Onlara yeni yola başlamaq, ona xətt seqmentləri və əyrilər əlavə etmək və onu bağlamaq üçün operatorlar daxildir.

* Path-painting operatorları yolu rənglə doldurur, onun boyunca bir xətt çəkir və ya kəsmə sərhədi kimi istifadə edir.

* Digər rəsm operatorları müəyyən özünü təsvir edən qrafik obyektləri rəngləyir. Bunlara nümunə götürülmüş şəkillər, həndəsi olaraq müəyyən edilmiş kölgələr və öz növbəsində qrafik operatorların ardıcıllığını ehtiva edən bütün məzmun axınları daxildir.

* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* İşarələnmiş məzmun operatorları daha yüksək səviyyəli məntiqi məlumatı məzmun axınındakı obyektlərlə əlaqələndirirlər. Bu məlumat məzmunun göstərilən görünüşünə təsir göstərmir; sənəd mübadiləsi üçün PDF istifadə edən proqramlar üçün faydalıdır.


## İstinadlar ##

* [PDF Fayl Format: Əsas Struktur](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)

* [PDF - Vikipediya](https://en.wikipedia.org/wiki/PDF)

* [PDF İstinad - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)


