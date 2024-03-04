{
  "date": "2019-11-25",
  "keywords": [
"jpeg failą",
"jpeg failo formatas",
"kas yra jpeg failas",
"failą",
"jpeg pavyzdys",
"jpeg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG – vaizdo failo formatas",
  "description": "Sužinokite apie JPEG failo formatą ir API, kurios gali kurti ir atidaryti JPEG failus.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-ltg"
}
},
  "lastmod": "2020-08-08"
}

## Kas yra JPEG failas? ##

JPEG yra vaizdo formatas, kuris išsaugomas naudojant nuostolingo glaudinimo metodą. Išvesties vaizdas dėl suspaudimo yra kompromisas tarp saugojimo dydžio ir vaizdo kokybės. Vartotojai gali reguliuoti suspaudimo lygį, kad pasiektų norimą kokybės lygį, tuo pačiu sumažindami saugyklos dydį. Vaizdo kokybei įtakos turi nežymiai, jei vaizdui taikomas glaudinimas 10:1. Kuo didesnė suspaudimo vertė, tuo didesnis vaizdo kokybės pablogėjimas.

## Failo formato specifikacijos ##

JPEG vaizdo failo formatą standartizavo Jungtinė fotografijos ekspertų grupė, taigi ir pavadinimą JPEG. Fotografinių vaizdų saugojimo ir perdavimo internete formatas buvo pasirinktas. Beveik visose operacinėse sistemose dabar yra peržiūros priemonės, palaikančios JPEG vaizdų vizualizavimą, kurie dažnai saugomi ir su JPG plėtiniu. Net žiniatinklio naršyklės palaiko JPEG vaizdų vizualizavimą. Prieš pereinant prie JPEG failo formato specifikacijų, reikia paminėti bendrą JPEG kūrimo veiksmų procesą.

### JPEG glaudinimo žingsniai ###

**Transformacija:** spalvoti vaizdai iš RGB paverčiami skaisčio / spalvingumo vaizdais (akis jautri šviesumui, o ne spalvingumui, todėl spalvingumo dalis gali prarasti daug duomenų ir todėl gali būti labai suspausta.

**Demyninis mėginių ėmimas:** Žemyninis mėginių ėmimas atliekamas spalvotam komponentui, o ne skaisčio komponentui. Apatinė atranka atliekama santykiu 2:1 horizontaliai ir 1:1 vertikaliai (2 val. 1 V). Taigi vaizdo dydis sumažėja, nes y komponentas neliečiamas, todėl vaizdo kokybė nepablogėja.

**Tvarkymas grupėse:** kiekvienos spalvos komponento pikseliai suskirstyti į 8 × 2 pikselių grupes, vadinamas duomenų vienetais, jei eilučių arba stulpelių skaičius nėra 8 kartotinis, apatinė eilutė ir dešiniausi stulpeliai yra dubliuojami.

**Diskrečioji kosinuso transformacija:** Diskretinė kosinuso transformacija (DCT) taikoma kiekvienam duomenų vienetui, kad būtų sukurtas 8 × 8 transformuotų komponentų žemėlapis. DCT apima tam tikrą informacijos praradimą dėl riboto kompiuterinės aritmetikos tikslumo. Tai reiškia, kad net ir be žemėlapio bus šiek tiek prarasta vaizdo kokybė, tačiau ji paprastai yra maža.

**Kvantifikavimas:** kiekvienas iš 64 transformuotų duomenų vieneto komponentų yra padalintas iš atskiro skaičiaus, vadinamo jo kvantavimo koeficientu (QC) ir suapvalinamas iki sveikojo skaičiaus. Čia informacija prarandama negrįžtamai, o didelis QC sukelia daugiau nuostolių. Apskritai dauguma JPEG įrenginių leidžia naudoti JPEG standarto rekomenduojamas QC lenteles.

**Kodavimas:** 64 kiekvieno duomenų vieneto kvantuoti transformuoti koeficientai (kurie dabar yra sveikieji skaičiai) yra užkoduoti naudojant RLE ir Huffman kodavimo derinį.

**Antraštės pridėjimas:** paskutinis veiksmas prideda antraštę ir visus naudojamus JPEG parametrus bei išveda rezultatą.

JPEG dekoderis naudoja atvirkštinius veiksmus, kad sukurtų originalų vaizdą iš suglaudinto.

### Failo struktūra ###

JPEG vaizdas vaizduojamas kaip segmentų seka, kur kiekvienas segmentas prasideda žymekliu. Kiekvienas žymeklis prasideda 0xFF baitu, po kurio eina žymeklio vėliavėlė, nurodanti žymeklio tipą. Naudingoji apkrova, po kurios yra žymeklis, skiriasi priklausomai nuo žymeklio tipo. Toliau pateikiami įprasti JPEG žymeklių tipai:

|Trumpas pavadinimas|baitai|naudinga apkrova|vardas|komentarai
---|---|---|---|---|
|SOI|0xFF, 0xD8|nėra|Vaizdo pradžia|
|S0F0|0xFF, 0xC0|kintamas dydis|Rėmelio pradžia|
|S0F2|0xFF, 0xC2|kintamas dydis|Rėmelio pradžia|
|DHT|0xFF, 0xC4|kintamas dydis|Apibrėžkite Huffman lenteles|
|DQT|0xFF, 0xDB|kintamas dydis|Apibrėžkite kvantavimo lentelę (-es)|
|DRI|0xFF, 0xDD|4 baitai|Nustatyti pakartotinio paleidimo intervalą|
|SOS|0xFF, 0xDA|kintamas dydis|Nuskaitymo pradžia|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|nėra|Paleisti iš naujo|
|APPn|0xFF, 0xE//n//|kintamo dydžio|Konkrečios programos|
|COM|0xFF, 0xFE|kintamas dydis|Komentuoti|
|EOI|0xFF, 0xD9|nėra|Vaizdo pabaiga|

Entropija užkoduotuose duomenyse po bet kurio 0xFF baito koduotuvas įterpia 0x00 baitą prieš kitą baitą, kad neatsirastų žymeklio ten, kur jo nėra, ir taip išvengiama kadravimo klaidų. Dekoderiai turi praleisti šį 0x00 baitą. Ši technika, vadinama [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (žr. JPEG specifikacijų skyrių F.1.2.3), taikoma tik entropijos koduotiems duomenims, o ne žymeklio naudingosios apkrovos duomenims. Tačiau atkreipkite dėmesį, kad entropija koduoti duomenys turi keletą savo žymenų; konkrečiai Reset žymekliai (0xD0–0xD7), kurie naudojami atskirti nepriklausomus entropija koduotų duomenų gabalus, kad būtų galima lygiagrečiai dekoduoti, ir koduotuvai gali laisvai įterpti šiuos atstatymo žymeklius reguliariais intervalais (nors ne visi koduotuvai tai daro).

