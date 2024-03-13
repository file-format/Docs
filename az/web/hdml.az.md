{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Əl Cihazı İşarələmə Dil Faylı",
  "description": "HDML fayl formatı və HDML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-azl"
}
},
  "lastmod": "2021-08-21"
}

## HDML faylı nədir?

.hdml (Əl Cihazı İşarələmə Dili) uzadılmasına malik fayl əl kompüterləri, smartfonlar və məlumat ekranı cihazları kimi portativ elektron cihazlar üçün veb səhifələr yaratmaq üçün işarələmə dilidir. HDML-in [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) dilinin uzantısı olduğu deyilir. HDML HTML-yə bənzəyir, lakin PDA, mobil telefonlar və s. kimi kiçik displeyləri olan simsiz və əl cihazları üçün. O, mühüm təsir kimi çıxış etdiyi WML ilə əvəz olundu.

## HDML Fayl Format - Ətraflı Məlumat

HDML, HTML-ə bənzər işarələmə etiketlərinə əsaslanan əl cihazları üçün işarələmə dilidir. HDML standartlaşdırma üçün W3C-yə təqdim edildi, lakin heç vaxt standart olmadı. Bununla belə, onun fayl formatının spesifikasiyası istinad üçün [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) saytında mövcuddur. [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) tərtibatçının arayışı üçün əlçatandır və nümunə tətbiqin inkişafı üçün istifadə edilə bilər.

## HDML elementləri

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


