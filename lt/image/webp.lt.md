{
  "date": "2019-10-11",
  "keywords": [
"webp failą",
"webp failo formatas",
"kas yra webp failas",
"failą",
"webp pavyzdys",
"webp failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP – „Google“ rastrinio vaizdo failo formatas",
  "description": "Sužinokite apie WEBP failo formatą ir API, kurios gali kurti ir atidaryti WEBP failus.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra WEBP failas?

Google pristatytas WebP yra modernus rastrinio žiniatinklio vaizdo failo formatas, pagrįstas nenuostolingu ir nuostolingu glaudinimu. Tai užtikrina tą pačią vaizdo kokybę ir žymiai sumažina vaizdo dydį. Kadangi dauguma tinklalapių naudoja vaizdus kaip efektyvų duomenų atvaizdavimą, WebP vaizdų naudojimas tinklalapiuose leidžia greičiau įkelti tinklalapius. Google teigimu, WebP vaizdai be nuostolių yra 26 % mažesnio dydžio, palyginti su [PNGs](/image/png/), o WebP nuostolingi vaizdai yra 25–34 % mažesni nei panašūs [JPEG](/image/jpeg/) vaizdai. Vaizdai lyginami pagal struktūrinio panašumo (SSIM) indeksą tarp WebP ir kitų vaizdo failų formatų. WebP yra [WebM](https://en.wikipedia.org/wiki/WebM) daugialypės terpės sudėtinio rodinio formato seserinis projektas.

## WebP funkcijų apžvalga ##

WebP vaizduose naudojamas glaudinimo procesas, pagrįstas juos supančių blokų pikselių numatymu, todėl pikseliai turi būti naudojami kelis kartus viename faile. Jis palaiko animuotus vaizdus ir tikimasi, kad ateityje palaikys daugiau funkcijų. Google padarė prieinamą kodavimo ir dekoderio šaltinio kodą [online](https://developers.google.com/speed/webp/download), kad jį būtų galima naudoti kur reikia. WebP vaizdas palaiko:

* **Prarastas glaudinimas:** nuostolingas glaudinimas pagrįstas [VP8](https://en.wikipedia.org/wiki/VP8) rakto kadro kodavimu. VP8 yra vaizdo glaudinimo formatas, kurį sukūrė On2 Technologies kaip VP6 ir VP7 formatų įpėdinį.

* **Nenuostolingas glaudinimas:** be nuostolių glaudinimo formatą sukūrė WebP komanda.

* **Skaidrumas:** 8 bitų alfa kanalas naudingas grafiniams vaizdams. Alfa kanalas gali būti naudojamas kartu su nuostolingu RGB – funkcija, kuri šiuo metu nepasiekiama su jokiu kitu formatu.

* **Animacija:** palaiko tikros spalvos animuotus vaizdus.

* **Metaduomenys:** gali turėti EXIF ir XMP metaduomenis (pavyzdžiui, naudojami fotoaparatuose).

* **Spalvų profilis:** gali turėti įdėtą ICC profilį.


Lossy WebP glaudinimas naudoja nuspėjamąjį kodavimą vaizdui koduoti, tą patį metodą, kurį naudoja VP8 vaizdo kodekas, kad suglaudintų vaizdo įrašų pagrindinius kadrus. Nuspėjamasis kodavimas naudoja gretimų pikselių blokų reikšmes, kad nuspėtų reikšmes bloke, o tada užkoduoja tik skirtumą.

Kad būtų galima tiksliai atkurti naujus pikselius, be nuostolių WebP glaudinimas naudoja jau matytus vaizdo fragmentus. Jis taip pat gali naudoti vietinę paletę, jei nerandama įdomių atitikmenų.

## Dokumento formatas ##

WebP failo formatas yra pagrįstas RIFF (resursų mainų failo formato) dokumento formatu. WebP konteineris palaiko daugiau ir daugiau funkcijų, nei turi tik vieną vaizdą, užkoduotą kaip VP8 rakto rėmelį. Pagrindinis RIFF failo elementas yra dalis, kurią sudaro:


|Laukas|Aprašymas
---|---|
|Chunk FourCC: 32 bitai|ASCII keturių simbolių kodas, naudojamas gabalo identifikavimui
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-ltng
|Rykio naudingoji apkrova: gabalo dydžio baitai|Duomenų naudingoji apkrova. Jei gabalo dydis yra nelyginis, pridedamas vienas užpildymo baitas ~-~-, kuris turėtų būti 0 ~-~-
|ChunkHeader ('ABCD')|Naudojama atskirų dalių FourCC ir Cunk Size antraštėms apibūdinti, kur ABCD yra FourCC, skirtas gabalui. Šio elemento dydis yra 8 baitai.

### WebP antraštė ###

WebP failo antraštė yra tokia:

* RIFF antraštė – 32 bitai, atstovaujantys ASCII simbolius „R“, „I“, „F“, „F“

* Failo dydis – 32 bitai (uint32), reiškiantis failo dydį baitais, pradedant nuo 8 poslinkio. Didžiausia šio lauko vertė yra 2^32 atėmus 10 baitų, taigi viso failo dydis yra daugiausia 4 GiB minus 2 baitai .

* „WEBP“ – 32 bitai, atstovaujantys ASCII simbolius „W“, „E“, „B“ „P“


### Prarastas failo formatas ###

WebP atvaizdai naudoja nuostolingo failo formatą, jei vaizdas pagrįstas nuostolinga kodavimu ir nereikalauja jokių išplėstinių / išplėstinių funkcijų, tokių kaip skaidrumas, animavimas, alfa ir kt. Praradę vaizdai yra mažesni ir juos palaiko ir senesnės programos.

Šiuo atveju WebP failą sudaro:

* 12 baitų WebP failo antraštė

* VP8 gabalas


[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) iliustruoja VP8 bitų srauto formato specifikacijas.

### Failo formatas be nuostolių ###

Šis išdėstymas naudojamas, kai vaizdas yra pagrįstas beprasmiu kodavimu ir nereikia papildomų funkcijų, kurias suteikia išorinis formatas. Tačiau senesnės programos gali nesugebėti nuskaityti tokių failų.

Šiuo atveju WebP failą sudaro:

* 12 baitų WebP failo antraštė

* VP8L gabalas


## Nuorodos Nr.

* [WebP kūrėjo nuoroda – pateikė Google](https://developers.google.com/speed/webp/)

* [WebP failo formatas – pagal Vikipediją](https://en.wikipedia.org/wiki/WebP)


