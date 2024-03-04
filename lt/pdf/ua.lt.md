{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/UA failo formatas",
  "description": "Sužinokite apie PDF / UA failo formatą ir API, kurios gali kurti ir atidaryti PDF / UA failus.",
  "linktitle": "PDF/UA",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-u-lta"
}
},
  "lastmod": "2019-09-10"
}

# Kas yra PDF/UA failas? #

PDF / UA buvo paskelbtas kaip [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) 2012 m. rugpjūčio mėn. ir yra pirmasis išsamus visuotinai prieinamų PDF dokumentų reikalavimų rinkinio apibrėžimas. Sąvoka visuotinai prieinama reiškia supratimą, kad [PDF](/pdf/) dokumente esanti informacija turėtų būti vienodai ir nepriklausomai prieinama visiems apskritai, o ypač žmonėms su negalia. PDF/UA standarto įvedimas gali būti laikomas pagrindiniu žingsniu kuriant įrankius ir programas, kad būtų galima kurti ir skaityti PDF turinį.

## Failo formato reikalavimai ##

PDF/UA pagrinde yra tam tikrų reikalavimų, kurie veikia kaip šio standarto esmė. Iš esmės jie yra pagrįsti PDF žymėjimu, o tai reiškia, kad visi PDF / UA dokumentai turi būti tinkamai pažymėti. Taip pat reikalaujama, kad žymos būtų semantiškai tinkamos ir logiška tvarka. Tai užtikrina, kad galutinis dokumentas, sukurtas naudojant PDF / UA specifikacijas, yra patikimesnis ir prieinamesnis. Dėl to PDF autoriai gali suabejoti, ar jiems reikia žinoti viską apie visus tokius reikalavimus? Laimei, taip nėra, nes PDF / UA atitikties įrankiai prisiima atsakomybę už PDF pridėjimą ir pasiekiamumo išsaugojimą.

Toliau pateikiami PDF/UA failo formato reikalavimai.

* Turinys skirstomas vienu iš dviejų būdų: prasmingas turinys ir artefaktai, pvz., dekoratyviniai puslapio elementai. Visas reikšmingas turinys turi būti pažymėtas ir integruotas į visų dokumento žymų struktūros medį. Kita vertus, artefaktus tereikia pažymėti kaip tokius.

* Prasmingas turinys turi būti pažymėtas žymomis ir kartu su kitomis dokumento žymomis sukurti pilną struktūros medį.

* Prasmingas turinys turi būti pažymėtas atitinkamomis semantinėmis žymomis.

* Dokumento žymų sukurtas struktūros medis turi atspindėti dokumento loginę skaitymo tvarką.

* Galima naudoti tik standartines žymas, apibrėžtas PDF 1.7; jei naudojamos kitos žymos, vaidmens priskyrimo įraše turi būti įrašyta, kurią standartinę žymą kiekviena iš jų atstovauja.

* Informacija negali būti perteikiama naudojant vien vaizdines priemones (pvz., kontrastą, spalvą ar padėtį puslapyje).

* Draudžiama mirgėti, mirksėti ar mirksėti turiniui, nei kaip „JavaScript“ valdomų efektų, nei kaip vaizdo įrašų, įterptų į PDF, dalis.

* Turi būti suteiktas dokumento pavadinimas ir dokumentas turi būti nustatytas taip, kad pavadinimas (o ne failo pavadinimas) būtų rodomas lango pavadinime.

* Turi būti pažymėta viso turinio kalba, o kalbos pakeitimai turi būti aiškiai pažymėti.


## PDF/UA atitiktis Nr.

PDF/UA standartas apibrėžia turinio, skaitytuvų ir pagalbinių technologijų specifikacijas. Šie trys aspektai yra susieti vienas su kitu, remiantis dokumento turiniu. Atitikties reikalavimai kiekvienam iš jų yra tokie, kaip nurodyta toliau.

## Atitinkami failai ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Atitinkantys skaitytojai ##

Atitinkantis skaitytojas turi laikytis PDF 1.7 specifikacijose nustatytų taisyklių. Konkrečiai, jis turėtų palaikyti:

* visos žymos, atributai ir pagrindinės reikšmės, nurodytos prieinamumui. Ji taip pat turėtų turėti galimybę apdoroti ir pateikti skaitmeninius parašus, komentarus ir pasirenkamą turinį.

* apdoroti ir pateikti skaitmeninius parašus, komentarus ir pasirenkamą turinį

* naršyti dokumentą įvairiomis priemonėmis


## Atitinkama pagalbinė technologija ##

Atitinkama pagalbinė technologija turi palaikyti PDF / UA funkcijas. Tai apima, pavyzdžiui, turinio ir skaitytuvo funkcijas ir turėtų leisti naršyti pagal puslapių etiketes, dokumento struktūrą arba kontūrą. Tai taip pat turėtų leisti vartotojui nepaisyti numatytojo naršymo mastelio.

## Nuorodos Nr.

* [PDF/UA – Vikipedija](https://en.wikipedia.org/wiki/PDF/UA)

* [PDF/UA trumpai](https://pdfa.org/pdfua-in-a-nutshell/)


