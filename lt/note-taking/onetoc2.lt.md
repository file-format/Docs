{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 – „Microsoft OneNote“ failo formatas",
  "description": "Sužinokite apie ONETOC2 failo formatą ir API, kurios gali kurti ir atidaryti ONETOC2 failus.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-lt2"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

Kai kuriate bloknotą OneNote 2016, jis automatiškai išsaugomas nauju 2010–2016 m. failo formatu. Šio formato jums reikės, jei norite, kad visos OneNote 2016 funkcijos, pvz., matematikos lygtys ir susietos pastabos, veiktų tinkamai.

## ONETOC2 failo formatas ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### Failo struktūra ###

Versijų saugyklos failas PRIVALO prasidėti **Antraštės** struktūra. Likusi failo dalis yra padalinta į baitų blokus, kur kiekvieno bloko dydis ir struktūra nurodomi jį nurodančioje srityje. Blokas pasiekiamas, jei jį nurodo struktūra **Antraštė** arba laukas kitame pasiekiamame bloke. Duomenų, nepriklausančių **Antraštės** struktūrai, ir bet kokių pasiekiamų blokų BŪTINA nepaisyti.

Visos struktūros yra sulygiuotos ant 1 baito ribų. Visi sveikieji skaičiai yra pasirašyti, jei nenurodyta kitaip. Visi laukai yra [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), jei nenurodyta kitaip.

#### Antraštė ####

ONE failo antraštė susideda iš dalių, kuriose yra skirtingi unikalūs ID ir laukai, skirti failo informacijai pateikti, kaip nurodyta toliau:

`guidFileType (16 baitų): GUID, nurodantis versijų saugyklos failo tipą. PRIVALO būti viena iš toliau pateiktos lentelės reikšmių.

|Failo formatas | Reikšmė
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

guidFile (16 baitų): GUID, nurodantis šio versijų saugyklos failo tapatybę. TURI būti unikalus visame pasaulyje.

guidLegacyFileVersion (16 baitų): PRIVALO būti {00000000-0000-0000-0000-000000000000} ir PRIVALO būti ignoruojamas.

`guidFileFormat (16 baitų): GUID, nurodantis, kad failas yra versijų saugyklos failas. TURI būti {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

ffvLastCodeThatWroteToThisFile (4 baitai): Nepaženklintas sveikasis skaičius. Priklausomai nuo failo tipo, PRIVALO būti viena iš reikšmių šioje lentelėje.

|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 baitai): sveikasis skaičius be ženklo. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.


|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvNewestCodeThatHasWrittenToThisFile (4 baitai): Nepaženklintas sveikasis skaičius. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.
:


|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvOldestCodeThatMayReadThisFile (4 baitai): Nepaženklintas sveikasis skaičius. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.


|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Nuorodos Nr.

* [[MS-ONESTORE] – „OneNote“ failo formatas](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote – Vikipedija](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


