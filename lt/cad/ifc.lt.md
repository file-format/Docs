{
  "date": "2020-03-16",
  "keywords": [
"IFC failas",
"Formatas",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie IFC failų formatą ir API, kurios gali kurti ir atidaryti IFC failus.",
  "title": "IFC failo formatas",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-ltc"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra IFC failas?

Failai su IFC plėtiniu reiškia Industry Foundation Classes (IFC) failų formatą, kuris nustato tarptautinius pastatų objektų ir jų savybių importo ir eksportavimo standartus. Šis failo formatas užtikrina skirtingų programinės įrangos programų sąveiką. Šio failo formato specifikacijas sukūrė ir prižiūri buildingSMART International kaip duomenų standartą. Galutinis IFC failo formato tikslas yra pagerinti komunikaciją, produktyvumą, pristatymo laiką ir kokybę per visą pastato gyvavimo ciklą.

Dėl nustatytų standartų, skirtų įprastiems statybų pramonės objektams, sumažėja informacijos praradimas perduodant iš vienos programos į kitą. IFC gali saugoti daugelio skirtingų profesijų (architekto, elektros, ŠVOK, konstrukcijų, reljefo ir kt.) geometrijos, skaičiavimo, kiekių, patalpų valdymo, kainodaros ir tt duomenis.

## Trumpa istorija ##

IFC iniciatyvos 1994 m. ėmėsi Autodesk, siekdama paremti integruotą taikomųjų programų kūrimą, įskaitant tokias įmones kaip Honeywell, Butler Manufacturing ir AT&T. 1995 m. narystė buvo atidaryta visiems, o pavadinimas pakeistas į Tarptautinį sąveikos aljansą. Ne pelno siekiančios organizacijos tikslas buvo paskelbti pramonės fondo klasę (IFC) kaip AEC produkto modelį. 2005 m. pavadinimas vėl buvo pakeistas ir dabar jį prižiūri buildSMART.

## IFC failo formatas ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Kartkartėmis buvo atlikti keli nedideli pakeitimai, kurie buvo įtraukti į specifikacijas kaip priedai. Toliau pateikiamas įvairių failų specifikacijų versijų, kurios anksčiau buvo viešai paskelbtos, sąrašas.

* IFC4 Add2 (2016) IFC4 Add1 (2015)

* IFC4 (2013 m. kovo mėn.) ifcXML2x3 (2007 m. birželis)

* IFC2x3 (2006 m. vasario mėn.) ifcXML2, skirtas IFC2x2 add1 (RC2)

* IFC2x2 1 priedas (2004 m. liepos mėn.) ifcXML2, skirtas IFC2x2 (RC1)

* IFC 2x2IFC 2x priedas 1ifcXML1, skirtas IFC2x ir

* IFC2x priedas 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


Naujausios IFC failo formato specifikacijų versijos visada pasiekiamos buildingSMART svetainėje ir kūrėjas turėtų pasikonsultuoti su jais dėl bet kokio tipo programų, kurias planuoja kurti. Rašant šį straipsnį, 4 versijos specifikacijos yra naujausios internete.

### IFC duomenų failų formatai ###

IFF failo formatas palaiko duomenų mainus tarp programų, naudojančių skirtingus formatus, kaip nurodyta toliau:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Šis failo formatas turi .ifc failo plėtinį ir yra dažniausiai naudojamas IFC formatas.

**IFC-XML:** Tai XML failo formato IFC versija, kurią siunčianti programa gali sugeneruoti tiesiogiai pagal ISO 10303-28 struktūrą, dar vadinamą STEP-XML. Laikoma, kad IFC-XML failo formatas tinkamas XML įrankių sąveikai. Palyginti su IFC failo formatu, IFC-XML yra 300–400% didesnis.

**IFC-ZIP:** Tai [ZIP](/compression/zip/) suglaudinta IFC arba IFC-XML versija, kur vienas iš šių failų yra pagrindinis ZIP archyvo katalogas. Šis formatas suglaudina .ifc failą 60–80 %, o .ifc XML failą – 90–95 %.

### IFC architektūra ###

IFC specifikacija apima terminus, sąvokas ir duomenų specifikacijų elementus, atsirandančius naudojant statybos ir pastatų valdymo pramonės sektoriaus disciplinas, amatus ir profesijas. Sąvokose ir sąvokose naudojami paprasti angliški žodžiai, duomenų specifikacijose esantys duomenų elementai atitinka pavadinimų suteikimo tvarką.

tipų, objektų, taisyklių ir funkcijų duomenų elementų pavadinimai prasideda priešdėliu Ifc ir tęsiasi angliškais žodžiais CamelCase pavadinimų sutartyje (be pabraukimo, pirmoji žodžio raidė didžiosiomis raidėmis); atributų pavadinimai objekte atitinka CamelCase pavadinimų suteikimo susitarimą be priešdėlio; ypatybių rinkinio apibrėžimai, kurie yra šio standarto dalis, prasideda priešdėliu Pset_ ir tęsiasi angliškais žodžiais CamelCase pavadinimų sutartyje; kiekių rinkinio apibrėžimai, kurie yra šio standarto dalis, prasideda priešdėliu Qto_ ir tęsiasi angliškais žodžiais CamelCase pavadinimų sutartyje.

IFC duomenų schemos architektūra apibrėžia keturis konceptualius sluoksnius, kiekviena atskira schema priskiriama tiksliai vienam koncepciniam sluoksniui.

**Išteklių sluoksnis** – žemiausias sluoksnis apima visas individualias schemas su išteklių apibrėžimais, į šiuos apibrėžimus neįeina visuotinai unikalus identifikatorius ir jie negali būti naudojami nepriklausomai nuo apibrėžimo, deklaruoto aukštesniame lygyje;

**Pagrindinis sluoksnis** – kitame sluoksnyje yra branduolio schema ir pagrindinių plėtinių schemos, kuriose yra bendriausi objektų apibrėžimai, visi pagrindiniame arba aukščiau apibrėžti objektai turi pasauliniu mastu unikalų ID ir pasirinktinai savininko bei istorijos informaciją;

**Sąveikumo sluoksnis** – kitas sluoksnis apima schemas, kuriose yra objektų apibrėžimų, būdingų bendram produktui, procesui ar išteklių specializacijai, naudojamai keliose disciplinose. Tie apibrėžimai paprastai naudojami mainams tarp domenų ir statybos informacijai dalytis;

**Domeno sluoksnis** – aukščiausias sluoksnis apima schemas, kuriose yra objektų apibrėžimų, kurie yra tam tikrai disciplinai būdingų produktų, procesų ar išteklių specializacija. Tie apibrėžimai paprastai naudojami keičiantis domene ir dalijantis informacija.

## Nuorodos Nr.

* [Industry Foundation Classes – pagal Vikipediją](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


