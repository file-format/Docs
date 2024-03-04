{
  "date": "2019-12-16",
  "keywords": [
"XLS",
"failą",
"pratęsimas",
"Dokumento formatas",
"Excel",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra XLS failas ir API, kurios gali juos sukurti ir atidaryti.",
  "title": "Kas yra XLS failo formatas? Mokykitės iš failų formatų ekspertų!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-lts"
}
},
  "lastmod": "2019-12-16"
}

## Kas yra XLS failas?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Trumpa istorija

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* 8 versija (išleista su Office 97): VBA buvo pristatyta kaip standartinė kalba ir pirmą kartą šioje versijoje buvo pašalintos natūralios kalbos etiketės. Ji taip pat pirmą kartą pristatė sąvaržėlių biuro asistentą.

* 9 versija (išleista kartu su „Office 2000“): 9 versijoje buvo atlikti tik nedideli pakeitimai, kai sąvaržėlės biuro asistentas vienu metu galėjo laikyti kelis objektus, kurių anksčiau nebuvo įmanoma.

* 10 versija (išleista kartu su „Office XP“): šioje versijoje nebuvo pastebimų patobulinimų.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS failo formato specifikacijos ##

Duomenys yra išdėstyti XLS faile kaip dvejetainiai srautai sudėtinio failo forma, kaip aprašyta Microsoft [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx) dokumente.

#### Srautas ir antrinis srautas ####

Darbaknygę vaizduoja darbaknygės srautas. Kiekvienas darbaknygės darbalapis yra pavaizduotas antriniais srautais. Be to, jame yra diagramos lapo posrautas, makro lapo posrautas arba dialogo lapo posrautas, kuris seka pasauliniu posūkiu. Kiekvienas dvejetainis srautas arba antrinis srautas, kuriame yra darbaknygės duomenų, PRIVALO būti parašytas kaip dvejetainių įrašų serija.

#### Įrašas ####

Informacija apie darbaknygės funkcijas saugoma kaip įrašas, kuris yra kintamo ilgio baitų seka. Dvejetainis įrašas susideda iš šių trijų komponentų:

**Įrašo tipas:** Įrašo tipas yra dviejų baitų beženklis sveikasis skaičius, nurodantis, kokio tipo informaciją nurodo įrašas ir kaip sutvarkyta ir struktūrizuota šiam įrašui būdingų įrašo duomenų struktūra. Įrašo tipo reikšmės TURI būti vertės iš įrašų sąrašo (2.3 skirsnis) arba įrašas PRIVALO naudoti būsimą įrašo architektūrą (2.1.6 skirsnis).

**Įrašo dydis**: įrašo dydis yra dviejų baitų be ženklo sveikasis skaičius, nurodantis baitų skaičių, nurodantį bendrą įrašo duomenų dydį. Įrašo dydis TURI būti didesnis arba lygus 0 ir TURI būti mažesnis arba lygus 8224.

**Įrašo duomenys:** Įrašo duomenų komponente yra laukai, atitinkantys konkretų įrašo tipą ir apimantys likusią įrašo dalį. Tam tikro įrašo tipo laukų tvarka ir struktūra nurodyta atitinkamame to įrašo tipo skyriuje. Įrašo duomenų komponento dydis TURI būti lygus įrašo dydžiui. Įrašo duomenų komponento laukuose gali būti paprastos reikšmės, reikšmių masyvai, kelių laukų struktūros, laukų masyvai ir struktūrų matricos.

#### Langelių lentelė ####

Langeliai yra pagrindiniai darbaknygės blokai, kuriuose saugomas darbaknygės turinys, pvz., tekstas, formulės ir skaitmeniniai duomenys. Ląstelės saugo saugomų duomenų įrašą naudodamos duomenų struktūrą, vadinamą langelių lentele. Pati langelių lentelė saugoma įrašų sekoje, atitinkančioje specifikacijų dokumente apibrėžtas CELLTABLE taisykles. Jį sudaro eilučių blokai, kuriuose eilutės yra išdėstytos eilučių blokais. Kiekviename eilučių bloke yra eilutės nuo pirmosios eilutės su duomenimis iki paskutinės eilutės su duomenimis.

Duomenys arba eilutės formatavimas išsaugomas kiekvieno eilutės bloko eilutės įraše. Kiekvienas langelis, kuriame yra duomenų arba atskiro langelio formatavimo, vaizduojamas įrašu. Su langeliu susietas formatavimas gali būti gaunamas iš atskirų langelių formatavimo, eilutės formatavimo, stulpelių formatavimo arba numatytojo langelio formato. Formatavimo eiliškumas yra atskirų langelių formatavimas su didžiausia pirmenybe, tada eilutės formatavimas, tada stulpelio formatavimas ir numatytasis langelio formatas. Langeliai, kuriuose nėra duomenų ir nėra individualaus formatavimo, neišsaugomi.

#### Formulės ####

Formulė yra reikšmių, langelių nuorodų, pavadinimų, funkcijų arba operatorių seka langelyje, kurie kartu sukuria naują reikšmę. Formulės saugomos tokenizuotame vaizde, vadinamame išnagrinėtomis išraiškomis. Išanalizuota išraiška vykdymo metu konvertuojama į tekstinę formulę, kad būtų galima rodyti ir redaguoti naudotoją. Ląstelių formules nurodo formulės įrašas. Masyvo formules nurodo masyvo įrašas. Bendrinamos formulės nurodomos ShrFmla įraše.

#### Diagramos ####

Diagramos lape nurodoma diagrama, grafika, rodanti duomenis arba ryšius tarp duomenų rinkinių vaizdine forma, ir diagramos duomenų talpykla, trūksta vietinės diagramos duomenyse naudojamų duomenų kopijos arba jei yra nuorodų į išorinius. duomenų šaltiniai sugedę. Diagramoje nurodomos vienos arba dviejų ašių grupės, ašių rinkinys, pagal kurį brėžiami diagramos duomenys, ir diagramoje nurodytas serijų, tendencijų linijų ir klaidų juostos rinkinys. Kiekviena ašių grupė nurodo nuo vienos iki keturių diagramų grupių, kurios nurodo vizualizacijos tipą, naudojamą duomenims rodyti. Kiekviena serija, tendencijų linija ir klaidų juosta nurodo diagramos grupę, su kuria ji susieta.

#### Metaduomenys ####

Metaduomenys yra papildomi duomenys, susieti su konkrečiu langeliu arba jo turiniu. Metaduomenys įrašomi į BIFF8 tik būsimiems išplėtimo tikslams.

#### Suvestinės lentelės ####

PivotTable yra šaltinio duomenų apibendrinimo mechanizmas, siekiant gauti tų duomenų paskirstymo apžvalgą. PivotTable taikomi šaltinio duomenų stulpeliai tampa laukais, kuriuos galima naudoti duomenims apibendrinti. Kai PivotTable šaltinio duomenys yra OLAP šaltinio duomenys, OLAP hierarchijos ir kai kurie kiti OLAP objektai tampa PivotTable laukais.
PivotTable susideda iš dviejų pagrindinių dalių: PivotCache ir PivotTable rodinio. Gali būti keli PivotTable rodiniai, pagrįsti viena ne OLAP PivotCache.

#### Stiliai ####

Šioje apžvalgoje aprašoma, kaip nurodoma lapo (1) langelių formatavimo ir apsaugos informacija. Langelių formatavimą sudaro keli ypatybių rinkiniai:

* Šrifto ypatybės (pusjuodis, kursyvas, šrifto spalva, šrifto dydis ir kt.)

* Užpildymo savybės (priekinio plano spalva, fono spalva, raštas, gradientas ir kt.)

* Lygiavimo ypatybės (lygiavimas kairėje, centre, dešinėje ir kt.)

* Kraštinės savybės (kairė, dešinė, viršuje, apačioje, stora arba plona, spalva ir tt)

* Skaičių formatavimo ypatybės (data, laikas, skaitmenų po kablelio skaičius ir kt.)

* Apsaugos savybės (užrakintos, paslėptos ir kt.)


Šios savybės, kaip visuma, apibūdina, kaip rodomas ir spausdinamas tam tikras langelis.

## Nuorodos Nr.

* [[MS-XLS] – „Excel“ dvejetainio failo formato struktūra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] – sudėtinio failo dvejetainio failo formatas](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


