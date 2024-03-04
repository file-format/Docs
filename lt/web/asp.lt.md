{
  "date": "2019-10-11",
  "keywords": [
"asp",
"asp failą",
"asp failo formatas",
"asp failo tipas",
"failą",
"tipo",
"kas yra asp failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASP – aktyvaus serverio puslapių failo formatas",
  "description": "Sužinokite, kas yra ASP failas ir API, kurios gali juos sukurti ir atidaryti.",
  "linktitle": "ASP",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-ltp"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ASP failas?

ASP reiškia Active Server Pages, kuri yra tinklalapių kūrimo sistema. Tai leidžia vidiniam serveriui vykdyti kompiuterio kodą, kad būtų galima aptarnauti žiniatinklio užklausas. Kai žiniatinklio naršyklė sugeneruoja ASP failo užklausą, serveris nuskaito failą ir vykdo bet kokį jame esantį kodą / scenarijų, kad sugeneruotų **[HTML](/web/html/)** rezultatą, kuris grąžinamas naršyklei parodyti.

Skirtingai nuo HTML puslapių, kurie yra statiniai serverio aptarnaujami puslapiai, ASP failai vykdymo metu generuoja dinaminį turinį, kuris gali apimti duomenų užklausas iš duomenų bazės. ASP puslapiuose paprastai naudojamas .asp plėtinys, o ne .html. Kadangi kodas / scenarijus ASP faile vykdomas serverio pusėje, užklausą pateikusi naršyklė nemato kodo, naudoto kuriant teikiamą puslapį. Visos šiuolaikinės naršyklės gali rodyti sugeneruotus puslapius. Sukurti naudojant Microsoft technologiją, puslapiai, sukurti naudojant ASP, yra talpinami Microsoft Internet Information Services (IIS) serveriuose.

## Trumpa ASP failo formato istorija
ASP buvo peržiūrėtas tik keletą kartų, kol jį pakeitė ASP.NET, kuris yra modernesnis ir efektyvesnis serverio puslapių kūrimo ir valdymo būdas. Pagal numatytuosius nustatymus ASP palaikymas yra įtrauktas kartu su interneto informacijos paslaugomis (IIS). ASP buvo paskelbta trimis skirtingomis versijomis su kiekvienos iš jų patobulinimais.

* ASP 1.0 buvo išleistas 1996 m. gruodžio mėn. kaip IIS 3.0 dalis

* ASP 2.0 buvo išleistas 1997 m. rugsėjo mėn. kaip IIS 4.0 dalis

* ASP 3.0 buvo išleistas 2000 m. lapkritį kaip IIS 5.0 dalis


## ASP funkciniai objektai

ASP failai naudoja serverio objektus, kad apdorotų vartotojų užklausas ir generuotų išvesties puslapius, kurie bus pateikti vartotojams. Kiekvienas objektas turi rinkinių, savybių ir metodų rinkinį užklausoms ir atsakymams apdoroti. Šie objektai apima:

### Užklausa objekto

Kai naršyklė prašo serverio puslapio, tai vadinama užklausa. Užklausos objektas naudojamas informacijai iš lankytojo gauti.

### Atsakymo objektas

ASP atsako objektas naudojamas siunčiant išvestį vartotojui iš serverio.

### Serverio objektas

ASP serverio objektas naudojamas pasiekti serverio ypatybes ir metodus. Tai leidžia prisijungti prie duomenų bazių (ADO), failų sistemos ir naudoti serveryje įdiegtus komponentus.

### Seanso objektas

Seanso objektas yra tarsi nuoroda tarp vartotojo naršyklės, prašančios puslapio iš serverio, ir paties serverio. Tai pasiekiama naudojant ASP sukurtą slapuką, kuris siunčiamas į vartotojo kompiuterį. Seanso objektas saugo informaciją apie vartotojo seansą arba keičia nustatymus. Informacija saugoma seanso objektas yra bendrinamas visuose programos puslapiuose. Įprasta informacija, saugoma seanso kintamuosiuose, yra pavadinimas, ID ir nuostatos. Serveris kiekvienam naujam vartotojui sukuria naują seanso objektą ir sunaikina seanso objektą pasibaigus seansui.

### Programos objektas

Programos objektas turi informaciją, kuri bus naudojama daugelyje programos puslapių (pvz., duomenų bazės ryšio informacija). Informaciją galima pasiekti iš bet kurio puslapio. Taip pat informaciją galima keisti vienoje vietoje, o pakeitimai automatiškai atsispindės visuose puslapiuose. Programos objektas naudojamas saugoti ir pasiekti kintamuosius iš bet kurio puslapio, kaip ir seanso objektas.

### ASPERror objektas

ASPERror objektas buvo įdiegtas ASP 3.0 ir yra prieinamas IIS5 ir vėlesnėse versijose. ASPERror objektas naudojamas išsamiai informacijai apie bet kokią klaidą, atsirandančią ASP puslapio scenarijuose, rodyti.

**Pastaba:** ASPERror objektas sukuriamas, kai iškviečiamas Server.GetLastError, todėl informaciją apie klaidą galima pasiekti tik naudojant Server.GetLastError metodą.

## Nuorodos

* [ASP – W3C](https://www.w3schools.com/asp/default.asp)

* [Paprastų ASP puslapių kūrimas](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


