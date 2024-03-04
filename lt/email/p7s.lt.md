{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7S failas – skaitmeniniu būdu pasirašytas el. pašto pranešimas",
  "description": "Sužinokite apie P7S failo formatą ir API, kurios gali kurti ir atidaryti P7S failus.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-lts"
}
},
  "lastmod": "2022.01.31"
}

## Kas yra P7S failas?

P7S failas yra skaitmeninis parašas, gaunamas su skaitmeniniu parašu pasirašytu el. Šio failo buvimas kaip el. laiško priedas patvirtina, kad el. laiškas išsiųstas iš autentiško šaltinio. Taip užtikrinama, kad siuntėjo kompiuteryje įdiegtas el. pašto pasirašymo sertifikatas. Kai toks pasirašytas el. laiškas siunčiamas iš vartotojo kompiuterio, prie jo pridedamas P7S failas, kuriame yra siuntėjo vardas. El. pašto programos, palaikančios pasirašytus el. laiškus, gali matyti siuntėjo informaciją.

## P7S failo formatas – daugiau informacijos

S/MIME (saugūs/daugiafunkciniai interneto pašto plėtiniai) P7S failuose yra informacija paprasto teksto formatu, kuris yra suprantamas žmonėms. El. pašto programos, tokios kaip Microsoft Outlook, Apple Mail ir Mozilla Thunderbird, palaiko skaitmeniniu būdu pasirašytą informaciją iš S/MIME el. El. laiško pasirašymas patvirtina siuntėjo tapatybę ir praneša gavėjui, kad pranešimas yra autentiškas. Kai el. laiškai atsisiunčiami iš el. pašto programų (arba kaip [EML](/email/eml/), arba [MSG](/email/msg/)), šie P7S failai yra pridedami prie šių el. laiškų.

P7S faile yra ši informacija:

 * Laiško kilmės šaltinis
 * Siuntimo data ir laikas,
 * Nesvarbu, ar jis buvo pakeistas perdavimo metu

Ši informacija įterpta naudojant viešojo rakto kriptografijos standarto Nr. 7 (PKCS7) technologiją, skaitmeniniu būdu prijungiant šifruotus parašus prie el. laiško.

## Nuorodos Nr.

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


