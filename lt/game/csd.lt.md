{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie CSD Steam Game Data Backup File formatą ir API.",
  "title" : "CSD failo formatas – „Steam“ žaidimų duomenų atsarginės kopijos failas",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd-lt",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Kas yra CSD failas?

CSD failas yra žaidimų atsarginės kopijos failas, sukurtas žaidimų paslaugos **Steam**, leidžiantis vartotojams atsisiųsti ir tvarkyti **Valve** žaidimus. Jame yra atsarginių duomenų, susijusių su žaidimais, kurie gali būti naudojami ištrintam žaidimui atkurti. Steam gali atkurti žaidimą iš CSD failo tik tuo atveju, jei žaidimas buvo atsisiųstas, įdiegtas ir pataisytas per Steam. Norėdami atkurti žaidimą iš CSD failo, naudokite parinktį Steam → Backup and Restore Gamesteam ir pasirinkite failą.

## CSD failo formatas – daugiau informacijos

CSD failo formato vidinė struktūra nėra viešai prieinama, o jo failo formato specifikacijos kūrėjui nepasiekiamos. CSD failai pateikiami kartu su CSM ir ISS failais, kurie taip pat yra Steam žaidimų failų formatai.

### Kur rasti Steam atsarginių kopijų failų?

Visus Steam atsarginių kopijų failus galite rasti šiose vietose:

 * C:\Programų failai (x86)\Steam\steamapps\common\<game name> \ :
 * \cfg\ – tinkintos konfigūracijos ir konfigūracijos scenarijai
 * \downloads\ – tinkintas kelių žaidėjų žaidimų turinys
 * \maps\ – pasirinktiniai žemėlapiai, kurie buvo įdiegti arba atsisiųsti kelių žaidėjų žaidimo metu
 * \medžiagos\ – tinkintos tekstūros ir apvalkalai
 * \SAVE\ – vieno žaidėjo išsaugoti žaidimai

Tačiau trečiųjų šalių sukurtų žaidimų vieta gali būti skirtinga ir ją nustato žaidimo kūrėjas.

### Atkūrimas iš CSD atsarginės kopijos failo

Įdiekite Steam ir prisijunkite prie tinkamos Steam paskyros (daugiau instrukcijų rasite Steam diegimas)
 * Paleiskite Steam.
 * Viršutiniame kairiajame Steam programos kampe spustelėkite Steam.
 * Pasirinkite Kurti atsargines kopijas ir atkurti žaidimus...
 * Pasirinkite Atkurti ankstesnę atsarginę kopiją
 * Naršykite iki žaidimo atsarginių failų vietos
 * Tęskite per Steam langus, kad įdiegtumėte reikiamus žaidimus.

## Nuorodos

 * [Steam atsarginės kopijos funkcijos naudojimas](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

