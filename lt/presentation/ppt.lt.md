{
  "date": "2019-12-13",
  "keywords": [
"ppt failą",
"ppt failo formatas",
"kas yra ppt failas",
"failą",
"ppt pavyzdys",
"ppt failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PPT failo formatą ir API, kurios gali kurti ir atidaryti PPT failus.",
  "title": "PPT – PowerPoint failo formatas",
  "linktitle": "PPT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pp-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PPT failas?

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. PPT faile gali būti kelių skirtingų tipų informacijos, pvz., teksto, ženklelių, vaizdų, daugialypės terpės ir kitų įterptųjų OLE objektų. Microsoft nuo 2007 m. sukūrė naujesnį PowerPoint failo formatą, žinomą kaip [PPTX](/presentation/pptx/), kuris yra pagrįstas Office OpenXML ir skiriasi nuo šio dvejetainio failo formato. Kelios kitos taikomosios programos, tokios kaip OpenOffice Impress ir Apple Keynote, taip pat gali kurti PPT failus.

## Trumpa istorija ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. Stabilus dvejetainis formatas buvo bendrinamas kaip numatytasis PowerPoint 97-2003, skirta Windows. Dvejetainis failo formatas palaikomas skaitymui ir rašymui naujausiose PowerPoint versijose, įskaitant PowerPoint 2016.

## Failo formato specifikacijos ##

Nuo pat pristatymo PPT failo formatas buvo keletą kartų peržiūrėtas, kad būtų pridėta naujų funkcijų ir patobulinimų. Naujausios versijos specifikacijos yra 6.0 versijos, paskelbtos 2018 m. rugpjūčio mėn., specifikacijos, kurios neturėtų būti maišomos su tikruoju produkto numeriu PPT failo formatu, nes Microsoft nebeteikia šio formato pakeitimų.

### Failo formato apžvalga ###

Kai kurie pagrindiniai PPT failo formato komponentai yra šie:

#### Skaidrės ####

Naudotojo duomenys, tokie kaip formos, tekstas, animacija ir medija, pridedami prie pristatymo skaidrėje. Pristatyme gali būti viena ar kelios skaidrės, kurios rodomos kaip skaidrių demonstracija paleidžiant pristatymą. Pristatyme yra pagrindinės skaidrės ir pavadinimų pagrindinės skaidrės, kurios veikia kaip bendrų pristatymo skaidrių vaizdinių savybių šablonas. Taip pat yra pagrindinė pastabų skaidrė ir padalomosios medžiagos pagrindinė skaidrė, kuri atlieka panašią paskirtį ir suteikia bendras vaizdines visų pastabų skaidres ir visas spausdintas dalomąsias medžiagas.

#### Formos ####

Formos – tai objektai, leidžiantys naudotojams į skaidrę įtraukti įvairaus turinio kaip rezervuotos vietos formų, paveikslėlių ir grafikų. Formos pagrindinėje skaidrėje apibrėžia bendrus figūrų grupių duomenis.

#### Vietos žymenų formos ####

Tai yra specialūs vietos žymekliai, kurie naudojami kaip įvairių objektų konteineriai. Įvairios rezervuotos vietos formos gali būti naudojamos siekiant pateikti užuominų, kaip įterpti tam tikrų tipų figūras, pvz., lenteles ar diagramas. Skaidrėje rezervuotos vietos forma pritaikoma prie pagrindinės pagrindinės skaidrės, pavadinimo pagrindinės skaidrės arba pastabų pagrindinės skaidrės vaizdinių savybių.

#### Išoriniai objektai ####

Išoriniai objektai, pvz., įterptasis ir susietas garso įrašas, susietas vaizdo įrašas, įterptieji ir susieti OLE objektai ir hipersaitai, gali būti įterpti į skaidrę. Šie objektai gali būti naudojami susietiems objektams aktyvuoti, kad būtų galima pasiekti išorinius išteklius skaidrių demonstravimo metu.

### Failo formato struktūros ###

PowerPoint dvejetainius failų formatus sudaro šie srautai, atspindintys bendrą dokumento struktūrą ir duomenis.

* Dabartinis vartotojo srautas

* „PowerPoint“ dokumentų srautas

* Nuotraukų srautas

* Suvestinė informacija ir dokumentų santraukos informacija (neprivaloma)


Išsamias DOC failo formato specifikacijas galima rasti [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) ir jas reikia peržiūrėti toliau pateiktoje išsamioje dalyje paminėtuose skyriuose.

#### Dabartinis naudotojo srautas ####

Ji saugo paskutinio dokumentą atidariusio naudotojo įrašus, o jo pavadinimas turi būti Dabartinis vartotojas.

#### PowerPoint dokumentų srautas ####

Saugo visą informaciją apie PowerPoint pristatymą ir paaiškina jos išdėstymą bei turinį. Tai būtinas srautas, kurio pavadinimas TURI būti PowerPoint Document. Šio srauto turinys nurodomas aukščiausio lygio įrašų seka. Daliniai įrašų sekos tvarkos apribojimai nurodyti PersistDirectoryAtom ir UserEditAtom įrašuose.

Kaip sudėtinio rodinio įrašai, DocumentContainer, MainMasterContainer (2.5.3 skirsnis), HandoutContainer (2.5.8 skirsnis), SlideContainer (2.5.1 skirsnis) ir NotesContainer (2.5.6 skirsnis) įrašai yra sudėtinio rodinio įrašų medžio šaknis. ir atomų įrašai. Bet kuriame konteinerio įraše gali būti kitų įrašų, kurie nėra aiškiai nurodyti kaip antriniai įrašai. Nežinomi įrašai identifikuojami, kai RecordHeader struktūros lauke recType (2.3.1 skirsnis) yra reikšmė, nenurodyta RecordType sąraše (2.13.24 skirsnis). Į šiuos nežinomus įrašus PRIVALO būti nepaisoma ir GALI<1> išsaugoti. Nežinomus įrašus galima ignoruoti ieškant recLen baitų iš RecordHeader struktūros pabaigos.

Kiekvieną kartą, kai rašomas šis srautas, prie esamo srauto gali būti pridėti nauji aukščiausio lygio įrašai, vartotojo redagavimas arba visas srauto turinys gali būti pakeistas atnaujinta aukščiausio lygio įrašų seka. Jei visas srautas nepakeičiamas, visi anksčiau buvę aukščiausio lygio įrašai, apimantys bet kokį ankstesnį naudotojo redagavimą, gali būti pasenę dėl vėliau pridedamų aukščiausio lygio įrašų, sudarančių dabartinį naudotojo redagavimą.

#### Nuotraukų srautas ####

Tai pasirenkamas srautas, kuriame yra duomenų apie nuotraukas, esančias PowerPoint pristatyme. Jos pavadinimas PRIVALO būti Paveikslėliai. Šio srauto turinį nurodo OfficeArtBStoreDelay įrašas, kaip nurodyta [MS-ODRAW] 2.2.21 skyriuje.

#### Suvestinės informacijos srautas ####

Ji saugo statistiką apie dokumentą pagal Microsoft Office standartą. Suvestinės informacijos srauto pavadinimas turi būti \005SummaryInformation, kur \005 yra simbolis, kurio reikšmė yra 0x0005, o ne eilutės raidė \005. Šifruotiems dokumentams šis srautas TURI būti praleistas. Šio srauto turinys nurodytas [MS-OSHARED] 2.3.3.2.1 skyriuje.

#### Dokumento suvestinės informacijos srautas ####

Pasirenkamas srautas, kurio pavadinimas PRIVALO būti \005DocumentSummaryInformation, kur \005 yra simbolis, kurio vertė yra 0x0005, o ne eilutės raidė \005. Šifruotiems dokumentams šis srautas GALI būti praleistas<2>. Šio srauto turinys nurodytas [MS-OSHARED] 2.3.3.2.2 skyriuje.

#### Šifruotas suvestinės informacijos srautas ####

Pasirenkamas srautas, kurio pavadinimas PRIVALO būti EncryptedSummary. Šis srautas egzistuoja tik užšifruotame dokumente. Šio srauto turinys nurodytas [MS-OFFCRYPTO] 2.3.5.4 skyriuje.

#### Skaitmeninio parašo saugykla ####

Pasirenkama saugykla, kurios pavadinimas PRIVALO būti _xmlsignatures. GALI būti praleistas ir GALI būti ignoruojamas. Šios saugyklos turinys nurodytas [MS-OFFCRYPTO] 2.5.2 skyriuje.

#### Tinkinta XML duomenų saugykla ####

Pasirenkama saugykla, kurios pavadinimas PRIVALO būti MsoDataStore. Saugyklos turinys nurodytas [MS-OSHARED] 2.3.6 skyriuje.

#### Parašų srautas ####

Pasirenkamas srautas, kurio pavadinimas PRIVALO būti _signatures. Jį TURĖTŲ praleisti ir GALI būti ignoruojamas. Šio srauto turinys nurodytas [MS-OFFCRYPTO] 2.5.1 skyriuje.

## Nuorodos Nr.

* [PPT failo formato specifikacijos](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: „Office“ bendrieji duomenų tipai ir objektų struktūros](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] – „Office“ dokumentų kriptografijos struktūra](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint failų formatai](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


