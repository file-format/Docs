{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDM Faylı - Əl Cihazı İşarələmə Dil Faylı",
  "description": "HDM faylları yarada və aça bilən HDM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-azm"
}
},
  "lastmod": "2022-10-12"
}

## HDM faylı nədir?

HDM faylı Əl Cihazı İşarələmə Dilində (HDML) yaradılmış işarələmə dili veb səhifə faylıdır. O, [HTML](/web/html/) dilinə bənzər işarələmə teqlərini ehtiva edir, lakin smartfonlar və PDA-lar kimi əl elektron cihazları üçün nəzərdə tutulub. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) standartlaşdırma üçün W3C-yə təqdim edildi, lakin standart ola bilmədi. HDM W3 veb saytında mövcud olan [HDML](/web/hdml/) fayl formatı spesifikasiyalarına əsaslanır.

## HDM Fayl Format - Ətraflı Məlumat

HDM faylı əl cihazlarında vizual olaraq hazırlanmış veb-saytda göstərilən işarələmə etiketlərindən ibarətdir. HDM faylları HTML səhifələri üçün istifadə edilən HTTP protokolu əvəzinə HDTP (Əl Cihaz Nəqliyyat Protokolu) protokolundan istifadə edərək cihazlara kopyalanır.

## HDML fayl elementləri

Aşağıda HDML üçün iş vaxtı mühitini təmin edən və istifadəçi agenti adlanan bir sıra elementlər verilmişdir.

|Element|Təsvir|
---|---|
|Kartlar|Bu, HDML-in əsas tikinti blokudur və istifadəçiyə məlumat kartları ilə əlaqə saxlamağa imkan verir. |
|Decks|HDML kartları göyərtələrdə qruplaşdırılıb. HDML göyərtəsi URL [RFC1738] ilə təyin olunduğuna görə HTML səhifəsinə bənzəyir və serverdən tələb olunan və istifadəçi agenti tərəfindən keşlənmiş məzmun vahididir.|
|Actions|Hərəkətlər PREV, SOFT1-SOFT8 və HELP tipli ola bilər. Bunlar mücərrəddir və istifadəçi interfeysində istifadəçi agenti tərəfindən xüsusi şəkildə dəstəklənir.|
|Fəaliyyətlər|Fəaliyyət bir məntiqi funksiyanı yerinə yetirən əlaqəli kartlar qrupu kimidir. Bunlar bir və ya daha çox göyərtəni əhatə edə bilər. HDML naviqasiyası və vəziyyət modeli fəaliyyətlər ətrafında qurulub.|
|Tarixə əsaslanan naviqasiya|İstifadəçi agenti istifadəçiyə göstərilən kartların tarixçəsini saxlayır. Əldə edilən hər bir kart kart tarixçəsinə əlavə edilir. İstifadəçi agenti istifadəçiyə tarixdəki əvvəlki karta asanlıqla geri qayıtmağa imkan verir.|

## İstinadlar

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML Spesifikasiyaları - W3 Məktəbləri](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


