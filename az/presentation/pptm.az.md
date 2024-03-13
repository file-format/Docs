{
  "date": "2019-10-11",
  "keywords": [
"pptm faylı",
"pptm fayl formatı",
"pptm faylı nədir",
"fayl",
"pptm nümunəsi",
"pptm fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPTM - Makro-aktiv PowerPoint təqdimat faylı formatı",
  "description": "PPTM faylları yarada və aça bilən PPTM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "PPTM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ppt-azm"
}
},
  "lastmod": "2019-09-10"
}

PPTM genişləndirilməsi olan fayllar Microsoft PowerPoint 2007 və ya daha yüksək versiyaları ilə yaradılmış Makro-aktiv Təqdimat fayllarıdır. Onlar [PPTX](/presentation/pptx/) fayllarına bənzəyir, fərqi ilə yan tərəf makroları ehtiva edə bilsə də, onları icra edə bilmir. PPTM faylları onları Microsoft PowerPoint-də açmaq və məzmunu yeniləməklə redaktə edilə bilər. Digər oxşar format PPSM-dir, lakin o, standart olaraq yalnız oxunur və açıldığında slayd şousunu başlayır. PPTM, PPTX kimi, mətn, şəkillər, videolar, qrafiklər və digər əlaqəli materiallar kimi müxtəlif təqdimat elementləri üçün slaydlar ehtiva edir.

## Qısa tarix ##

PPTM file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Yeni fayl növü kiçik fayl ölçüləri, daha az korrupsiya dəyişiklikləri və yaxşı formatlaşdırılmış şəkillərin təqdim edilməsi kimi üstünlükləri əlavə etdi. 2000-ci ilin əvvəllərində Microsoft **Office Open XML** standartına uyğunlaşmaq üçün dəyişikliyə getməyə qərar verdi. 2007-ci ilə qədər bu yeni fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft Office-in yeni versiyalarında da davam etdirilir.

## Fayl Formatının Xüsusiyyətləri ##

Office Open XML fayl formatı ilə yaradılan fayllar, bütün tərkib faylları arasında əlaqə təmin edən digər fayllarla birlikdə XML faylları toplusudur. Bu kolleksiya əslində məzmununa baxmaq üçün çıxarıla bilən sıxılmış arxivdir. Bunu etmək üçün, sadəcə olaraq PPTM fayl uzantısının adını zip ilə dəyişdirin və məzmununu müşahidə etmək üçün onu çıxarın.

Aşağıdakı bölmələr bunların hər birinə bir qədər işıq salır.

### [Məzmun_Növləri].xml ###

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir. Aşağıda slayd hissəsi üçün məzmun növü verilmişdir:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Paketə yeni hissələrin əlavə edilməsi lazımdırsa, bu, yeni hissənin əlavə edilməsi və .rels faylları daxilində hər hansı əlaqənin yenilənməsi ilə edilə bilər. Nəzərə almaq lazımdır ki, belə bir dəyişiklik üçün Content_Types.xml də yenilənməlidir.

### \_rels (Qovluq) ###

Digər hissələr və paketdən kənar resurslar arasındakı əlaqələr əlaqələr hissəsi tərəfindən qorunur. Əlaqələr qovluğunda paket səviyyəli əlaqələri saxlayan tək XML faylı var. Təqdimat fayllarının əsas hissələrinə keçidlər bu faylda URI-lər kimi yer alır. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura ppt/presentation.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Bir və ya bir neçə əlaqənin mənbəyi olan sənədin hər bir hissəsinin öz əlaqələr hissəsi olacaq, burada hər bir belə əlaqə hissəsi hissənin \_rels alt qovluğunda yerləşir və adın adına '.rels' əlavə edilməklə adlandırılır. hissəsi. Əsas məzmun hissəsinin (presentation.xml) öz əlaqələr hissəsi (presentation.xml.rels) var. O, slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml kimi məzmunun digər hissələri ilə əlaqələri, həmçinin xarici keçidlər üçün URI-ləri ehtiva edir.

#### Açıq Münasibət ####

Açıq əlaqə üçün a-nın Id atributundan istifadə edərək mənbəyə istinad edilir<Relationship> element. Yəni mənbədəki İd hədəfə açıq istinadla birbaşa əlaqə elementinin İd-si ilə xəritələnir.

Məsələn, slaydda bu kimi hiperlink ola bilər:
```
<a:hlinkClick r:id#"rId2">
```
r:id#rId2 slayd üçün əlaqələr hissəsində aşağıdakı əlaqəyə istinad edir (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Gizli Münasibət ####

Gizli əlaqə üçün `-ə belə birbaşa istinad yoxdur<Relationship> ID`. Bunun əvəzinə istinad başa düşülür.

### ppt Qovluğu ###

Bu, Təqdimatın məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* slaydlar

* slideLayouts

* slideMasters


və aşağıdakı xml faylları:

* təqdimat.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## İstinadlar ##

* [[MS-PPTX] - PPTX Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


