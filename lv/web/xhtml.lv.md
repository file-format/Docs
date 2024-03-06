{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"paplašināms html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML — paplašināms hiperteksta iezīmēšanas valodas faila formāts",
  "description": "Uzziniet, kas ir XHTML faila formāts un API, kas var izveidot un atvērt XHTML failus.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir XHTML fails?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Šie faili ir labi piemēroti atvēršanai vai skatīšanai tīmekļa pārlūkprogrammā. XHTML tika izstrādāts tā, lai tas būtu vairāk strukturēts, mazāk skriptu, vispārīgs; izmantojot visas esošās XML iespējas un vairāk neatkarīgas no ierīcēm. XHTML nodrošina vispārēji vērtīgu elementu un atribūtu kopu ar paplašinājuma opcijām kombinācijā ar stila lapām. Atribūti tiek izmantoti no metadatu atribūtu kolekcijas. XHTML nodrošina elastību un pieejamību, pakārtojot visus **[HTML](/web/html/)** prezentācijas elementus stilu lapām. Stila lapas ir daudzpusīgākas nekā šie prezentācijas elementi. HTML 4.01, HTML5 un XHTML specifikācijas dinamiski izstrādā World Wide Web Consortium (W3C).

## Īsa XHTML faila formāta vēsture

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. Tomēr 2005. gadā tika izveidota darba grupa (WHATWG), kuras mērķis bija uzlabot parasto HTML neatkarīgi no XHTML. Galu galā WHATWG sāka strādāt pie HTML5 paralēli XHTML 2.

## XHTML faila formāts

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. XHTML faili ir balstīti uz XML, un to mērķis ir strādāt ar lietotāju aģentiem, kuru pamatā ir XML. XHTML faili atbilst XML. Standarta XML rīki tiek izmantoti, lai skatītu, rediģētu un apstiprinātus XHTML failus. HTML dokumenta objekta modelis vai XML dokumenta objekta modelis [DOM] atkarīgās lietojumprogrammas var darboties, izmantojot XHTML dokumentus. Šodien izvēloties XHTML, satura izstrādātāji var baudīt visas ar XML saistītās priekšrocības, neuztraucoties par sava satura saderību uz priekšu vai atpakaļ.

Saistītu elementu kopa veido moduli XHTML valodā. Veidlapu vai tabulu modulis var saturēt dažādus veidlapas vai tabulas elementus, ko var parādīt tīmekļa lapā. Modularizācijas mērķis bija izolēt HTML elementus daudzu saistīto elementu kopās. Lai satura izstrādātāji varētu izmantot moduļu izvēles priekšrocības dažāda veida ierīcēm. Turklāt moduļi ļauj lietotāju aģentiem atlasīt elementus, nezaudējot atbilstību XHTML standartam. XHTML parsēšanas prasības ir tādas pašas kā XML, savukārt HTML praktizē savas.

### Dokumenta atbilstība

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Dokumentu atbilstība ir divu veidu.

Stingri atbilstošs dokuments ir balstīts uz XML, un tam ir nepieciešami tikai šajā specifikācijā definētie obligātie pakalpojumi. XHTML failiem ir jāatbilst šādiem kritērijiem:

* Failam jāatbilst ierobežojumiem, kas noteikti DTD un B pielikumā.

* Faila bāzes elementam jābūt html.

* Faila pamatelementam ir jābūt XHTML nosaukumvietas deklarācijai, un tas jādefinē šādi:


```
http://www.w3.org/1999/xhtml.
```

* Pamatelementu var rakstīt šādi:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Agrāk par bāzes elementu ir jādeklarē DOCTYPE, kura publiskajam identifikatoram ir jāatsaucas uz vienu no trim dokumenta tipa definīcijām (DTD). Sistēmas identifikatoru var modificēt, lai tas atbilstu pašreizējām sistēmas konvencijām.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML dokumentos nav nepieciešams norādīt XML deklarācijas visos dokumentos; tomēr satura izstrādātāji tiek mudināti izmantot XML deklarācijas visos savos XHTML dokumentos. Šīs deklarācijas ir obligātas, ja dokumenta rakstzīmju kodējums atšķiras no UTF-8 /16, vai arī regulējošā protokolā nav norādīts kodējums. Šis XHTML dokumenta piemērs definē XML deklarācijas

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Atbilstošam lietotāja aģentam ir jāatbilst šādiem noteikumiem:

* XHTML dokumenta parsēšanu un novērtēšanu veic lietotāja aģents, kas nodrošina tā atbilstību XML 1.0 rekomendācijai.

* Lietotāja aģenta apstiprināšanas gadījumā tam ir jāpārbauda dokumentu derīgums tiem norādītajiem DTD saskaņā ar XML. Ja lietotāja aģents XHTML failu apstrādā kā vispārīgu XML, ID tipa līdzekļi tiks atzīti kā fragmentu identifikatori.


Ja lietotāja aģents uzduras neatpazītam elementam, tam ir jāizpilda šādi obligātie kritēriji

* apstrādāt šī nezināmā elementa saturu

* ignorēt atribūtu un tā vērtību

* Izmantojiet atribūta vērtību, kas norādīta kā noklusējuma vērtība.


Ja lietotāja aģents saskaras ar entītijas atsauces deklarāciju, kas nav apstrādāta agrāk, tā ir jāapstrādā kā rakstzīmes (sākot ar zīmi &” un beidzot ar semikolu). Satura apstrādes laikā rakstzīmes vai rakstzīmju entītiju atsauces, kuras lietotāja aģents paredz, bet nav atveidojamas, var izmantot jebkuru alternatīvu renderēšanu, kas nodrošina līdzīgu nozīmi. Šādā gadījumā dokumentam jābūt attēlotam tā, lai lietotājam būtu skaidrs, ka renderēšanas process nav bijis normāls. Lai apstrādātu atstarpes, lietotāja aģentam definīcija jāmeklē no CSS rakstzīmēm [CSS2].

## XHTML atpakaļsaderība

The back ward compatibility of XHTML 1.  dokumenti labi pārzina HTML 4 lietotāju aģentus, ja tiek ievēroti atbilstošie noteikumi. XHTML 1.1 ir pilnībā saderīgs, izņemot rubīna anotācijas, lai gan HTML 4 pārlūkprogrammas tās parasti ignorē. XHTML 2.0 ir salīdzinoši mazāk saderīgs, tomēr problēma zināmā mērā ir novērsta, izmantojot skriptus.

## Atsauces

* [XHTML vēsture: no 1990. gadiem līdz mūsdienām](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


