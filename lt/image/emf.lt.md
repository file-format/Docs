{
  "date": "2019-10-11",
  "keywords": [
"emf failas",
"emf failo formatas",
"kas yra emf failas",
"failą",
"emf pavyzdys",
"emf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF – patobulintas metafailo formatas",
  "description": "Sužinokite apie EMF failų formatą ir API, kurios gali kurti ir atidaryti EMF failus.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra EMF failas?

**Patobulintas metafailo formatas (EMF)** grafinius vaizdus išsaugo nepriklausomai nuo įrenginio. EMF metafailus sudaro kintamo ilgio įrašai chronologine tvarka, kurie gali pateikti saugomą vaizdą, jį išnagrinėjus bet kuriame išvesties įrenginyje. Šie kintamo ilgio įrašai gali būti uždarų objektų apibrėžimai, piešimo komandos ir grafinės savybės, būtinos norint tiksliai atvaizduoti vaizdą. Kai įrenginys atidaro EMF metafailą naudodamas savo grafinę aplinką, pradinio vaizdo proporcijos, matmenys, spalvos ir kitos grafinės savybės išlieka tokios pačios, neatsižvelgiant į atidarymo įrenginio platformą.

## Trumpa istorija ##

1990 m. Microsoft sukūrė vaizdo failo formatą Windows Metafile ([WMF](/image/wmf/)), skirtą Microsoft Windows. Windows metafailai yra 16 bitų formatas, kuriame gali būti kai kurių taškinės schemos komponentų. WMF gali būti sudarytas iš vektorinės grafikos ir yra skirtas nešioti įvairioms programoms. 1993 m. Win32/GDI paskelbė patobulintą metafailą (EMF), naujesnę versiją, pasižyminčią didesniu lankstumu ir masteliu. EMF taip pat naudojamas kaip grafikos kalbos komandos spausdintuvo tvarkyklėms paleisti. Microsoft dabar rekomenduoja patobulintą metafailo formatą (EMF), o ne Windows formatą (WMF). Kai buvo pristatyta Windows XP, buvo išleista Enhanced Metafile Format Plus (EMF+) versija. Ši naujesnė versija suranda savo kelią nuosekliai suskirstydama GDI+ API skambučius, taip pat WMF/EMF įrašo skambučius į GDI. Yra gzip suglaudinta EMF versija, žinoma kaip EMZ.

## EMF metafailo formatas ##

Toliau pateikiami pagrindiniai patobulinto metafailo formato elementai:

* EMR_HEADER (versija, dydis, nuotraukos skiriamoji geba kuriant)

* GDI objektų lentelė

* Rezervuota paletė (neprivaloma)

* Metafailų įrašai, išdėstyti masyvo struktūroje (ypatybių nustatymai, apibrėžti objektai, piešimo komandos)

* EMR_EOF įrašas (paskutinis įrašas EMF metafaile)


## EMF versijos Nr.
* **Original**: originalioje versijoje nurodomas įrašas, būtinas norint išlaikyti originalų vaizdą ir išlaikyti jo nepriklausomą nuo įrenginio. Be to, palaiko įrašą, kuriame yra grafinių objektų ir piešimo komandų.

* **1 versija**: antroji EMF versija pagerino lankstumą ir įrenginio nepriklausomybę, pridėdama pikselių formato įrašą ir galimybę naudoti OpenGL komandą.

* **2 versija**: trečioji versija padidino tikslumą, pridedant metrinę sistemą, skirtą įrenginio paviršiaus atstumui matuoti, todėl įrašas tapo labiau keičiamas.


## Patobulinti metafailų įrašai ##

Metafailų įrašai yra išdėstyti masyvo forma. Šie įrašai turi ENHMETARECORD struktūrą ir kintamo ilgio. ENHMETARECORD nurodo duomenis, apibrėžiančius GDI funkcijas, kad būtų galima sukurti paveikslėlį naudojant patobulintą metafailo formatą. **ENHMETAHEADER** struktūra visada yra pirmasis šio formato įrašas. Šioje EMF antraštėje yra ši informacija.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Kiekviename metafaile turi būti bent vienas EMF įrašas. Informacija, perduodama iš vieno įrašo į kitą, priklauso nuo EML įrašų, todėl šie įrašai turi būti išdėstyti greta. Bet kuriame metafailo įraše, išskyrus EOF_record, to konkretaus įrašo ilgis nustatomas norint pereiti prie kito įrašo.

## Patobulintas metafailų kūrimas ##

Funkcija **CreateEnhMetaFile** naudojama patobulintam metafailui sukurti. Šios funkcijos argumentai naudojami vaizdo matmenims ir saugojimui diske / atmintyje. Be to, šiai funkcijai reikalingas įrenginio, kuriame vaizdas pasirodė pirmasis, matmuo (nuorodos įrenginys) ir atskaitos įrenginio (DC) kontekstas. Taigi, iškviečiant funkciją **CreateEnhMetaFile**, reikia pateikti argumentus, kaip tvarkyti šį DC. Funkcijos sintaksė yra tokia:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** rankena prie atskaitos įrenginio.

**lptoFilename:** failo pavadinimo žymeklis.

**lprc:** Rodyklė į ovalią struktūrą nurodo nuotraukos matmenis mm.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Patobulintos metafailų operacijos ##

Toliau pateikiami darbai, kuriuos galima atlikti naudojant patobulinto metafailo rankenėlę.

* Rodyti ir redaguoti išsaugotą paveikslėlį.

* Kurkite patobulintas metafailų kopijas.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Apibendrinkite spalvas paletėje.


## Grafiniai objektai ##

Piešimo ir tapybos operacijose grafikos objektus galima sukurti objektų kūrimo įrašais ir išsaugoti tolesniam naudojimui. EMR_SELECTOBJECT įrašas gali nuskaityti šiuos grafinius objektus naudodamas atkūrimo įrenginio kontekstą. Rašikliai, paletės, teptukai, spalvų erdvės, šriftai ir atsarginiai objektai yra kai kurie daugkartinio naudojimo objektų tipai.

## Baitų užsakymas ##

Little-endian formatas naudojamas duomenims saugoti metafailų įrašuose.

## Versija Nr.

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Išplėstinėse versijose yra numatyti OpenGL įrašai ir pasirenkamas vidinio pikselių formato aprašas. Pridedama matavimo priemonė mililitrais rodomiems matmenims.

## Nuorodos Nr.

* [Patobulinto formato metafailai | „Microsoft Docs“](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Patobulintas metafailo formatas ir specifikacijos](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


