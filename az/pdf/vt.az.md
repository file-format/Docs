{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/VT fayl formatı",
  "description": "PDF/VT fayl formatı və PDF/VT faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PDF/VT",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-v-azt"
}
},
  "lastmod": "2019-09-10"
}

# PDF/VT nədir? #

Standart olaraq 2010-cu ilin avqustunda [ISO 16612-2](https://www.iso.org/standard/46428.html) kimi nəşr olunan PDF/VT müxtəlif mühitlərdə dəyişən sənəd çapını (VDP) aktivləşdirmək üçün nəzərdə tutulub. Standart Dəyişən məlumatı və Transaksiya çapını standart üçün əsas edir. Dəyişən məlumat çapı məlumatın bir hissəsi məzmunun hər bir alıcısı üçün fərqli olduğu hallarda istifadə olunur. Tranzaksiya çapına fakturalar, çıxarışlar və faktura məlumatı ilə marketinq məlumatlarını birləşdirən digər sənədlər daxildir. Bu, şəkillərin, mətnin və digər məzmun növlərinin təkmilləşdirilmiş işlənməsi ilə nəticələnir. PDF/VT sənəd hissəsi metadata (DPM) konsepsiyasından istifadə etməklə Yüksək Həcmli Transaksiya Nəticəsi (HVTO) çap məlumatları üçün səhifələrin etibarlı və dinamik idarə olunmasına imkan verir. PDF/VT faylları Adobe Acrobat Viewer proqramında başqa komponent əlavə etmədən açıla bilər.

## Sənəd Hissəsinin İerarxiyası ##

Sənəd Hissəsi (DPart) İerarxiyası sənədin bütün səhifələrinə əsaslanan sənəd hissəsi qovşaqlarının ağac quruluşuna bənzəyir. Bu ağacın elementlərinə DPart qovşaqları deyilir. Hər bir daxili node digər DPart qovşaqlarını ehtiva edir və hər bir yarpaq qovşağı alıcı üçün bir və ya bir neçə səhifəni təyin edir. Əsasən, DPart iyerarxiyası sənədlərin ardıcıllığını və əlaqəsini və ya PDF/VT faylında sənədlərin patlarını təyin edir. DPart qovşaqlarının ağac strukturu PDF/VT sənədinin daxili məzmununu asanlıqla təmsil edir, çünki o, bir çox alıcı üçün alt sənədləri ehtiva edə bilər və hər bir sənəd hissəsi bir alıcının səhifələrinə uyğundur. PDF/VT fayllarında DPart iyerarxiyası tələb olunur.

## Sənəd Hissəsinin Metadatası (DPM) ##

Sənəd Hissəsinin Metaməlumatları (DPM) sənəd hissəsi iyerarxiyasının hər bir qovşağı ilə əlaqələndirilir və konkret alıcının alt sənədi və onun hissələri haqqında məlumat ötürmək üçün istifadə edilə bilər. Xüsusilə, DPM-də kodlaşdırılmış formada xüsusiyyətlər və ya alıcılar haqqında məlumat ola bilər.

## Uyğunluq Səviyyələri ##

PDF/VT aşağıdakı üç uyğunluq səviyyəsinə verilir. Bunların hamısı [PDF](/pdf/) 1.6-a əsaslanır.

* `PDF/VT-1` - O, PDF/X-4-ə əsaslanır və PDF sənədini göstərmək üçün tələb olunan bütün resursları ehtiva edir.

* `PDF/VT-2` - Çox fayl mübadiləsi üçün nəzərdə tutulmuş PDF/VT-2 sənədləri xarici çıxış niyyətlərinə, xarici məzmunlara və ya hər ikisinə istinad edə bilər. PDF/VT sənədi və onun bütün istinad edilən PDF faylları və xarici çıxış niyyətləri birlikdə PDF/VT-2 fayl dəsti adlanır. Acrobat 9 və bu funksiyanı dəstəkləyir.

* `PDF/VT-2s` - PDF/VT-2 canlı yayımını dəstəkləyir. Bu, verilənlərin seqmentləşdirilmiş hissələrini emal etməyə imkan verir.


## İstinadlar ##

* [PDF/VT - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/PDF/VT)

* [ISO 16612-2 Qrafik Texnologiya](https://www.iso.org/standard/46428.html)


