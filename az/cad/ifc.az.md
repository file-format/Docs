{
  "date": "2020-03-16",
  "keywords": [
"IFC faylı",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "IFC faylları yarada və aça bilən IFC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "IFC fayl formatı",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-azc"
}
},
  "lastmod": "2019-09-10"
}

## IFC faylı nədir?

IFC genişləndirilməsi olan fayllar tikinti obyektlərini və onların xassələrini idxal və ixrac etmək üçün beynəlxalq standartları müəyyən edən Sənaye Əsas Sinifləri (IFC) fayl formatına istinad edir. Bu fayl formatı müxtəlif proqram proqramları arasında qarşılıqlı əlaqəni təmin edir. Bu fayl formatı üçün spesifikasiyalar buildingSMART International tərəfindən Data Standard kimi işlənib hazırlanır və saxlanılır. IFC fayl formatının son məqsədi binanın həyat dövrü ərzində rabitə, məhsuldarlıq, çatdırılma müddəti və keyfiyyəti yaxşılaşdırmaqdır.

Tikinti sənayesində ümumi obyektlər üçün müəyyən edilmiş standartlara görə, bir tətbiqdən digərinə ötürülmə zamanı məlumat itkisini azaldır. IFC bir çox müxtəlif peşələr (memar, elektrik, HVAC, struktur, ərazi və s.) üçün həndəsə, hesablama, kəmiyyətlər, obyektlərin idarə edilməsi, qiymətlər və s. məlumatları saxlaya bilər.

## Qısa tarix ##

IFC təşəbbüsü 1994-cü ildə inteqrasiya olunmuş tətbiqlərin işlənib hazırlanmasını dəstəkləmək üçün Autodesk tərəfindən qəbul edilmiş və Honeywell, Butler Manufacturing və AT&T kimi şirkətləri əhatə etmişdir. 1995-ci ildə üzvlük hər kəsin üzünə açıldı və adı qarşılıqlı fəaliyyət üçün Beynəlxalq Alyans olaraq dəyişdirildi. Qeyri-kommersiya təşkilatının məqsədi AEC məhsul modeli kimi Sənaye Əsas Sinifini (IFC) dərc etmək idi. 2005-ci ildə ad yenidən dəyişdirildi və buildSMART indi onu qoruyur.

## IFC fayl formatı ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Zaman-zaman bir neçə kiçik dəyişikliklər baş verdi, o cümlədən əlavələr kimi spesifikasiyaların bir hissəsi edildi. Aşağıda keçmişdə açıqlanmış fayl spesifikasiyalarının müxtəlif versiyalarının siyahısı verilmişdir.

* IFC4 Add2 (2016) IFC4 Add1 (2015)

* IFC4 (mart 2013) ifcXML2x3 (iyun 2007)

* IFC2x3 (Fevral 2006) IFC2x2 add1 (RC2) üçün ifcXML2

* IFC2x2 Əlavə 1 (iyul 2004) IFC2x2 (RC1) üçün ifcXML2

* IFC 2x2IFC 2x Əlavə 1ifcXML1 IFC2x və

* IFC2x Əlavə 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


IFC fayl formatının spesifikasiyalarının ən son versiyaları həmişə buildingSMART veb saytında mövcuddur və tərtibatçı inkişaf etdirməyi planlaşdırdığı istənilən proqram növü üçün bunlarla məsləhətləşməlidir. Bu məqaləni yazarkən, versiya 4 spesifikasiyaları onlayn mövcud olan ən son xüsusiyyətlərdir.

### IFC Məlumat Fayl Formatları ###

IFF fayl formatı aşağıda sadalanan müxtəlif formatlardan istifadə edən proqramlar arasında məlumat mübadiləsini dəstəkləyir:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Bu fayl formatı .ifc fayl uzantısına malikdir və ən çox istifadə olunan IFC formatıdır.

**IFC-XML:** Bu, STEP-XML adlanan ISO 10303-28 strukturuna uyğun olaraq göndərici proqram tərəfindən birbaşa yaradıla bilən IFC-nin XML fayl formatı versiyasıdır. IFC-XML fayl formatı XML alətləri arasında qarşılıqlı fəaliyyət üçün uyğun hesab olunur. IFC fayl formatı ilə müqayisədə, IFC-XML ölçüsünə görə 300-400% daha böyükdür.

**IFC-ZIP:** Bu, IFC və ya IFC-XML-in [ZIP](/compression/zip/) sıxılmış versiyasıdır, burada bu fayllardan biri zip arxivinin əsas kataloqunu təşkil edir. Bu format .ifc faylını 60-80% və .ifc XML faylını 90-95% sıxışdırır.

### IFC Arxitektura ###

BMK spesifikasiyasına tikinti və obyektlərin idarə edilməsi sənayesi sektorunun fənlər, peşələr və peşələr daxilində istifadədən irəli gələn terminlər, anlayışlar və məlumat spesifikasiyası elementləri daxildir. Terminlər və anlayışlar sadə ingilis sözlərindən istifadə edir, verilənlərin spesifikasiyasındakı məlumat elementləri adlandırma konvensiyasına əməl edir.

tiplər, obyektlər, qaydalar və funksiyalar üçün məlumat elementi adları Ifc prefiksi ilə başlayır və CamelCase adlandırma konvensiyasında ingilis sözləri ilə davam edir (alt xətt yoxdur, sözün ilk hərfi böyük hərflə); obyekt daxilində atribut adları heç bir prefiks olmadan CamelCase adlandırma konvensiyasına əməl edir; bu standartın bir hissəsi olan əmlak dəsti tərifləri Pset_ prefiksi ilə başlayır və CamelCase adlandırma konvensiyasında ingilis sözləri ilə davam edir; Bu standartın bir hissəsi olan kəmiyyət dəsti tərifləri Qto_ prefiksi ilə başlayır və CamelCase adlandırma konvensiyasında ingilis sözləri ilə davam edir.

IFC-nin məlumat sxemi arxitekturası dörd konseptual təbəqəni müəyyən edir, hər bir fərdi sxem tam olaraq bir konseptual təbəqəyə təyin edilir.

**Resurs təbəqəsi** — ən aşağı səviyyə resurs təriflərini ehtiva edən bütün fərdi sxemləri ehtiva edir, bu təriflərə qlobal unikal identifikator daxil edilmir və daha yüksək səviyyədə elan edilmiş tərifdən asılı olmayaraq istifadə edilməməlidir;

**Əsas təbəqə** — növbəti təbəqəyə nüvə sxemi və ən ümumi obyekt təriflərini ehtiva edən əsas genişləndirmə sxemləri daxildir, əsas qatda və ya yuxarıda müəyyən edilmiş bütün obyektlər qlobal miqyasda unikal identifikatoru və istəyə görə sahib və tarix məlumatını daşıyır;

**Əlaqədarlıq səviyyəsi** — növbəti səviyyə bir neçə fən üzrə istifadə edilən ümumi məhsul, proses və ya resurs ixtisaslaşmasına xas olan obyekt təriflərini ehtiva edən sxemləri ehtiva edir, bu təriflər adətən domenlərarası mübadilə və tikinti məlumatlarının mübadiləsi üçün istifadə olunur;

**Domen qatı** — ən yüksək səviyyəyə müəyyən intizam üçün xas məhsullar, proseslər və ya resursların ixtisaslaşması olan obyekt təriflərini ehtiva edən sxemlər daxildir, bu təriflər adətən domendaxili mübadilə və məlumat mübadiləsi üçün istifadə olunur.

## İstinadlar ##

* [Sənaye Vəqfi Dərsləri - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


