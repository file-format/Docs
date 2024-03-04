{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portable Document Format (PDF) yra standartinis dokumentų atvaizdas, nepriklausomas nuo programinės įrangos, aparatinės įrangos ir OS. PDF standartai apima PDF/A, PDF/E, PDF/UA, PDF/VT ir PDF/X.",
  "title" : "PDF failo formatas – kas yra PDF failas?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
"weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) yra dokumento tipas, kurį Adobe sukūrė 1990 m. Šio failo formato tikslas buvo įdiegti standartą, skirtą dokumentų ir kitos informacinės medžiagos vaizdavimui tokiu formatu, kuris nepriklauso nuo taikomosios programinės įrangos, aparatinės įrangos ir operacinės sistemos. PDF failo formatas turi visas galimybes talpinti informaciją, pvz., tekstą, vaizdus, hipersaitus, formos laukus, raiškiąją mediją, skaitmeninius parašus, priedus, metaduomenis, geografines ypatybes ir 3D objektus, kurie gali tapti šaltinio dokumento dalimi.

Daugeliu atvejų esami dokumentai konvertuojami į PDF, o ne sukuriamas naujas PDF nuo nulio. Tačiau tai nereiškia, kad nėra programinės įrangos PDF failams kurti ar jais valdyti.

**(Ar turite ką nors papasakoti apie PDF failo formatą? Savo atradimus galite paskelbti [PDF File Format News](https://news.fileformat.com/t/PDF) skiltyje.)**

## PDF failo formatas – trumpa istorija

Greita laiko juosta apie [PDF file format](https://products.fileformat.com/pdf/), atsižvelgiant į laiko juostą, yra tokia:

**1993 m.** – Adobe Systems pateikė PDF specifikacijas nemokamai

**2008 m.** – PDF buvo išleistas kaip atviras standartas 2008 m. liepos 1 d., o Tarptautinė standartizacijos organizacija paskelbė **ISO 32000-1:2008**.

**2008 m.** – Adobe paskelbė viešąją patento licenciją pagal ISO 32000-1 formato nemokamas teises, skirtas visiems Adobe priklausantiems patentams, kurių reikia norint sukurti, naudoti, parduoti ir platinti PDF suderinamus diegimus.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. PDF 1.7, kuris tapo ISO 32000-1, apima kai kurias nestandartizuotas patentuotas technologijas, taip pat kaip Adobe XML Forms Architecture (XFA) ir JavaScript plėtinį, skirtą Acrobat. Tai buvo 2017 m. liepos 28 d., kai buvo paskelbtas PDF 2.0, žinomas kaip ISO 32000-2:2017, kuriame nėra jokių nestandartinių technologijų.

## PDF failo formato specifikacijos

PDF failas yra baitų rinkinys, kurį galima sugrupuoti į žetonus pagal sintaksės taisykles, apibrėžtas PDF specifikacijose. Kartą ar daugiau žetonų sujungiami, kad būtų sudaryti aukštesnio lygio sintaksiniai objektai, daugiausia objektai, kurie yra pagrindinės duomenų reikšmės, iš kurių kuriamas PDF dokumentas.

### PDF failų failų struktūra

PDF failo turinys faile išdėstytas tokia seka.

|Antraštė
|Kūnas
|Kryžminių nuorodų lentelė
|Priekabė

#### PDF failo antraštė ####

Nepriklausomai nuo PDF versijos, PDF failas prasideda antrašte, kurioje yra unikalus PDF identifikatorius ir formato versija, pvz., %PDF-1.x, kur x svyruoja nuo 1 iki 7.

#### Failo turinys ####

PDF failo turinį sudaro netiesioginių objektų seka, vaizduojanti dokumento turinį. Objektai, kaip aprašyta aukščiau, yra dokumento komponentai, pvz., šriftai, puslapiai ir atrinkti vaizdai. Pradedant nuo PDF 1.5, tekste taip pat gali būti objektų srautų, kurių kiekviename yra netiesioginių objektų seka.

#### Kryžminių nuorodų lentelė ####

Kryžminių nuorodų lentelėje yra informacija, leidžianti atsitiktine tvarka prieiti prie netiesioginių objektų faile, kad nereikėtų skaityti viso failo, norint rasti konkretų objektą. Lentelėje turi būti vienos eilutės įrašas kiekvienam netiesioginiam objektui, nurodant to objekto baitų poslinkį failo turinyje. (Pradedant PDF 1.5, dalis arba visa kryžminių nuorodų informacija gali būti įtraukta į kryžminių nuorodų srautus.

#### Failo anonsas ####

PDF failo anonsas leidžia atitinkančiam skaitytojui greitai rasti kryžminių nuorodų lentelę ir tam tikrus specialius objektus. Atitinkantys skaitytojai turėtų skaityti PDF failą nuo jo pabaigos. Paskutinėje failo eilutėje turi būti tik failo pabaigos žymeklis %%EOF. Dviejose ankstesnėse eilutėse turi būti po vieną eilutėje ir eilės tvarka, raktinis žodis startxref ir baitų poslinkis dekoduotame sraute nuo failo pradžios iki raktinio žodžio xref pradžios paskutinėje kryžminės nuorodos dalyje.

### PDF objektai ###

PDF faile yra keletas skirtingų tipų objektų, kurie yra šių tipų

* Būlio reikšmės – reiškia sąlyginę teisingą arba klaidingą

* Skaičiai – sveikieji ir realieji skaičiai

* Stygos – skliausteliuose yra simbolių

* Vardai – pradėkite nuo į priekį / simboliu, pvz., /ASomewhatLongerName rezultatas yra ASomewhatLongerName

* Masyvai – PDF palaiko vienmačius masyvus. Didesnių matmenų masyvai gali būti sukurti naudojant masyvus kaip įdėtus elementus

* Žodynai – objektų rinkinys kaip raktų-reikšmių poros. Jame gali būti nulis įrašų.

* Srautai – reiškia baitų seką, kuri taip pat gali būti neriboto ilgio

* Null Object – reiškia nulinę reikšmę


Gali būti ir kitų objektų, pvz., komentarų, kurie pateikiami su % ženklu ir gali turėti 8 bitų simbolių.

### Netiesioginiai objektai ###

Bet koks PDF failo objektas gali būti pažymėtas kaip netiesioginis objektas. Netiesioginiams objektams suteikiamas unikalus objekto identifikatorius, pagal kurį kiti objektai gali į jį kreiptis. Kryžminės nuorodos į juos išlaikomos rodyklės lentelėje ir pažymėtos raktiniu žodžiu xref, kuris eina po pagrindinio turinio ir pateikia kiekvieno netiesioginio objekto baitų poslinkį nuo failo pradžios.

### Linijiniai ir nelinijiniai PDF maketai ###

Atsižvelgiant į tikslines programas ir kitus veiksnius, PDF maketai skirstomi į Llnear ir nelinijinius.

Netiesiniai – nelinijiniai PDF failai naudoja mažiau vietos diske, palyginti su linijiniais PDF failais. PDF dokumento puslapiai yra išsklaidyti PDF faile, todėl nelinijiniai failai yra lėtesni, palyginti su linijiniais failais.

Linijinis PDF – nukreipti į internetines PDF peržiūros programas, linijiniai PDF failai yra sukurti taip, kad į diską būtų įrašomi linijiniu būdu. Tam nereikia naršyklės papildinių, kad visas dokumentas būtų įkeltas prieš pateikiant.

### Objektų apžvalga ###

Kaip minėta, PDF tekstas yra aukščiau paminėtų objektų rinkinys. PDF daugiausia yra pagrįstas PostScript be programavimo kalbų valdymo funkcijų, tokių kaip if ir loop komandos. Postscript kodo išduodamos komandos grafiniam turiniui generuoti yra renkamos ir ženklinamos kartu su bet kokiais dokumente nurodytais failais, grafika ar šriftais. Visas šis turinys kaupiamas viename faile, todėl gaunama sudėtinė PostScript išvestis.

#### Tekstas ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Grafika ####

Grafikos operatoriai, naudojami PDF turinio srautuose, apibūdina puslapių, kurie turi būti atkurti rastriniame išvesties įrenginyje, išvaizdą. Priemonės skirtos tiek spausdintuvams, tiek ekranams. Grafikos operatoriai sudaro šešias pagrindines grupes:

* Grafikos būsenos operatoriai manipuliuoja duomenų struktūra, vadinama grafikos būsena, pasauline sistema, kurioje vykdo kiti grafikos operatoriai. Grafikos būsena apima dabartinę transformacijos matricą (CTM), kuri vartotojo erdvės koordinates, naudojamas PDF turinio sraute, susieja išvesties įrenginio koordinates. Tai taip pat apima dabartinę spalvą, dabartinį kirpimo kelią ir daugelį kitų parametrų, kurie yra numanomi tapybos operatorių operandai.

* Kelio kūrimo operatoriai nurodo kelius, kurie apibrėžia formas, linijų trajektorijas ir įvairių rūšių regionus. Juose yra operatoriai, skirti pradėti naują kelią, pridėti prie jo linijos segmentus ir kreives ir jį uždaryti.

* Kelio piešimo operatoriai užpildo taką spalva, piešia brūkšnį išilgai jo arba naudoja jį kaip iškirpimo ribą.

* Kiti tapybos operatoriai piešia tam tikrus save apibūdinančius grafikos objektus. Tai apima atrinktus vaizdus, geometriškai apibrėžtus atspalvius ir ištisus turinio srautus, kuriuose savo ruožtu yra grafikos operatorių sekos.

* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* Pažymėto turinio operatoriai susieja aukštesnio lygio loginę informaciją su turinio srauto objektais. Ši informacija neturi įtakos pateikto turinio išvaizdai; tai naudinga programoms, kurios naudoja PDF dokumentų mainams.


## Nuorodos Nr.

* [PDF failo formatas: pagrindinė struktūra](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)

* [PDF – Vikipedija](https://en.wikipedia.org/wiki/PDF)

* [PDF nuoroda – „Adobe“](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)


