{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent failo formatas - BitTorrent failas",
  "description":"Sužinokite apie TORRENT failus ir API, kurios gali kurti ir atidaryti TORRENT failus.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent-lt",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas yra TORRENT failas?

TORRENT failas yra tekstinis failas, kurį BitTorrent ir kitos P2P (peer-to-peer) programos naudoja turiniui atsisiųsti ir keistis. Atsisiunčiamas turinys gali apimti dokumentus, vaizdo įrašus, žaidimus, filmus ir kitą internete pasiekiamą mediją. Tai apima metaduomenų informaciją apie atsisiunčiamos medijos turinį ir vietą. Programinė įranga, tokia kaip BitTorrent, naudoja informaciją iš šio failo, pvz., pavadinimą, failo dydį ir aplanko struktūrą duomenims atsisiųsti. Torrent failus galima konvertuoti į kitus failų formatus, pvz., [PDF](/pdf/) internete.

## Kas yra Torrenting? TORRENT failo formatas duomenų mainams

Torrenting yra duomenų failų keitimosi (atsiuntimo ir įkėlimo) koncepcija naudojant BitTorrent tinklą. Skirtingai nuo įprastų serverių, kuriuose duomenys įkeliami, kad kiti galėtų juos pasiekti ir atsisiųsti, torrent failai nuskaitomi ir siunčiami naudojant torrent tinklą. Kai vartotojas atidaro .torrent failą tokiose programose kaip BitTorrent, programinė įranga pradeda atsisiųsti failo turinį bitais. Jei keli vartotojai turi tą patį failą, BitTorrent padalija atsisiuntimus visiems vartotojams, kad pagreitintų atsisiuntimo procesą. Tuo pačiu metu failą atsisiunčiančio vartotojo kompiuteris taip pat tampa failo šaltiniu, siunčiančiu jį kitiems vartotojams, kurie taip pat atsisiunčia tą patį failą.

### TORRENT failo struktūra

Torrent failas yra failų sąrašo ir metaduomenų informacijos apie visas atsisiunčiamas failo dalis derinys. Jame yra ši informacija raktų pavidalu.

- announce – stebėjimo priemonės URL, kuris pranešamas kitiems lygiaverčiams, siekiant informuoti apie failo prieinamumą
- Informacija – susiejama su žodynu, kurio raktai priklauso nuo to, ar bendrinamas vienas ar keli failai:
  - "failai – failą atitinkančių žodynų sąrašas (tik tada, kai bendrinami keli failai). Kiekvienas žodynas turi šiuos raktus:"
- ilgis - failo dydis baitais.
- kelias - eilučių, atitinkančių pakatalogių pavadinimus, sąrašas, iš kurių paskutinis yra tikrasis failo pavadinimas
- ilgis – failo dydis baitais (tik tada, kai bendrinamas vienas failas)
- `vardas` – failo pavadinimas, kuriame failas turi būti išsaugotas
- gabalo ilgis – baitų skaičius gabale. Paprastai tai yra 28 KiB = 256 KiB = 262 144 B.
- gabalai – maišos sąrašas, kuris yra kiekvienos dalies SHA-1 maišos junginys.

## Ar „Torrenting“ yra saugus ir teisėtas?

Torrenting protokolas, skirtas keistis duomenimis tarp P2P vartotojų, yra saugus, nes tai tik priemonė dalytis bet kokio tipo failais. Taigi pats protokolas nėra nesaugus ar neteisėtas. Tačiau tinkle bendrinamame turinyje gali būti failų ar laikmenų, kurie gali pažeisti bendrinamų dokumentų teisinį statusą. Tokiu atveju keitimasis tokiais duomenimis gali sukelti teisinius veiksmus šalims, dalyvaujančioms viešai dalijantis tokiais failais.

## Nuorodos

* [TORRENT failas – wikipedia](https://en.wikipedia.org/wiki/Torrent_file)


