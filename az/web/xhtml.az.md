{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"genişləndirilə bilən html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML - Genişlənən Hipermətn İşarələmə Dili Fayl Format",
  "description": "XHTML fayl formatı və XHTML faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-azl"
}
},
  "lastmod": "2019-09-10"
}

## XHTML faylı nədir?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Bu fayllar veb brauzerdə açmaq və ya baxmaq üçün çox uyğundur. XHTML daha strukturlaşdırılmış, daha az skript, ümumi olmaq üçün nəzərdə tutulmuşdur; XML-in bütün mövcud imkanlarından və daha çox cihazdan müstəqil istifadə. XHTML üslub vərəqləri ilə birlikdə genişləndirmə seçimləri ilə ümumiyyətlə dəyərli elementlər və atributlar dəstini təmin edir. Atributlar metadata atributları kolleksiyasından istifadə olunur. XHTML bütün **[HTML](/web/html/)** təqdimat elementlərini üslub cədvəllərinə tabe etməklə çeviklik və əlçatanlıq təmin edir. Stil vərəqləri bu təqdimat elementlərindən daha çox yönlüdür. HTML 4.01, HTML5 və XHTML üçün spesifikasiyalar World Wide Web Consortium (W3C) tərəfindən dinamik şəkildə hazırlanır.

## XHTML Fayl Formatının Qısa Tarixi

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. Bununla belə, 2005-ci ildə XHTML-dən asılı olmayaraq adi HTML-ni təkmilləşdirmək məqsədi daşıyan işçi qrup (WHATWG) yaradıldı. WHATWG nəhayət, XHTML 2 ilə paralel olaraq HTML5 üzərində işləməyə başladı.

## XHTML fayl formatı

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. XHTML-dəki fayllar XML əsaslıdır və XML-ə əsaslanan istifadəçi agentləri ilə işləmək məqsədi daşıyır. XHTML faylları XML-ə uyğundur. Standart XML alətləri XHTML fayllarına baxmaq, redaktə etmək və təsdiqləmək üçün istifadə olunur. HTML Sənəd Obyekt Modeli və ya XML Sənəd Obyekt Modelindən [DOM] asılı proqramlar XHTML sənədləri vasitəsilə işləyə bilər. Bu gün XHTML-ə üstünlük verən məzmun tərtibatçıları məzmunlarının irəli və ya geri uyğunluğundan narahat olmadan XML-in bütün əlaqəli üstünlüklərindən istifadə edə bilərlər.

Əlaqədar elementlər dəsti XHTML-də modul qurur. Formalar və ya cədvəl modulu veb-səhifədə göstərilə bilən müxtəlif forma və ya cədvəl elementlərini ehtiva edə bilər. Modulizasiya HTML elementlərini çoxsaylı əlaqəli elementlər dəstlərinə təcrid etmək məqsədi daşıyırdı. Məzmun tərtibatçıları müxtəlif növ cihazlar üçün modul seçimindən yararlana bilsinlər. Bundan əlavə, modullar istifadəçi agentlərinə XHTML standartı ilə uyğunluğu itirmədən elementləri seçməyə imkan verir. XHTML-in təhlil tələbləri XML ilə eynidir, HTML isə özünü tətbiq edir.

### Sənədin Uyğunluğu

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Sənəd uyğunluğu iki növdür.

Ciddi Uyğun Sənəd XML əsaslıdır və yalnız bu spesifikasiyada müəyyən edilmiş məcburi xidmətlərə ehtiyac duyur. XHTML faylları üçün aşağıdakı meyarlar yerinə yetirilməlidir:

* Fayl DTD-lərdə və Əlavə B-də müəyyən edilmiş məhdudiyyətlərə uyğun olmalıdır.

* Faylın əsas elementi html olmalıdır.

* Faylın əsas elementi XHTML ad məkanı üçün bəyannaməni ehtiva etməlidir və aşağıdakı kimi müəyyən edilməlidir:


```
http://www.w3.org/1999/xhtml.
```

* Əsas element aşağıdakı kimi yazıla bilər:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Əsas elementdən əvvəl DOCTYPE elan edilməlidir, onun ictimai identifikatoru üç sənəd növü tərifindən (DTDs) birinə istinad etməlidir. Sistem identifikatoru mövcud sistem konvensiyalarına uyğun olaraq dəyişdirilə bilər.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML sənədlərində bütün sənədlərdə XML bəyannamələrinin göstərilməsinə ehtiyac yoxdur; lakin məzmun tərtibatçıları bütün XHTML sənədlərində XML bəyannamələrindən istifadə etməyə tələsirlər. Bu bəyannamə ya sənədin simvol kodlaşdırması UTF-8 /16-dan fərqli olduqda və ya heç bir kodlaşdırma idarəedici protokolla müəyyən edilmədikdə məcburidir. XHTML sənədinin aşağıdakı nümunəsi XML bəyannamələrini müəyyən edir

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Uyğun olan istifadəçi agenti aşağıdakı qaydaları yerinə yetirməlidir:

* XHTML sənədinin təhlili və qiymətləndirilməsi onun XML 1.0 Tövsiyəsinə uyğunluğunu təmin edən istifadəçi agenti tərəfindən həyata keçirilir.

* İstifadəçi agentinin təsdiqlənməsi halında, XML-ə uyğun olaraq istinad edilən DTD-lər üçün sənədlərin etibarlılığını yoxlamalıdır. XHTML faylı istifadəçi agenti tərəfindən ümumi XML kimi işləndikdə, ID tipinin xüsusiyyətləri fraqment identifikatorları kimi qəbul ediləcək.


İstifadəçi agenti tanınmayan elementə rast gələrsə, onun yerinə yetirməli olduğu məcburi meyarlar aşağıdakılardır.

* həmin naməlum elementin məzmununu emal edin

* atribut və onun dəyərinə məhəl qoymayın

* Defolt olaraq verilən atributun dəyərindən istifadə edin.


İstifadəçi agenti əvvəllər işlənməmiş bir quruma istinad bəyannaməsi ilə qarşılaşdıqda, o, simvollar kimi işlənməlidir (&” işarəsi ilə başlayıb nöqtəli vergüllə bitən). Məzmun emalı zamanı istifadəçi agenti tərəfindən proqnozlaşdırıla bilən, lakin göstərilə bilməyən simvollar və ya xarakter obyekti istinadları oxşar məna verən hər hansı alternativ renderdən istifadə edə bilər. Bu halda, sənəd istifadəçiyə göstərmə prosesinin normal olmadığını başa düşəcək şəkildə göstərilməlidir. Boşluğu emal etmək üçün istifadəçi agenti CSS simvollarından [CSS2] tərifinə baxmalıdır.

## XHTML geriyə uyğunluq

The back ward compatibility of XHTML 1.  düzgün qaydalara əməl olunarsa, sənədlər HTML 4 istifadəçi agentlərini yaxşı bilir. XHTML 1.1, HTML 4 brauzerləri tərəfindən ümumiyyətlə nəzərə alınmamasına baxmayaraq, yaqut annotasiyaları istisna olmaqla, tam uyğundur. XHTML 2.0 nisbətən az uyğun gəlir, buna baxmayaraq problem skriptin istifadəsi ilə müəyyən dərəcədə həll edilmişdir.

## İstinadlar

* [XHTML tarixi: 1990-cı illərdən bu günə](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


