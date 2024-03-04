{
  "date": "2020-03-16",
  "keywords": [
"STL failas",
"Formatas",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie STL failo formatą ir API, kurios gali kurti ir atidaryti STL failus.",
  "title": "STL failo formatas",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra STL failas?

STL, stereolitrografijos santrumpa, yra keičiamas failo formatas, vaizduojantis 3 dimensijos paviršiaus geometriją. Failo formatas yra naudojamas keliose srityse, pavyzdžiui, greitas prototipų kūrimas, 3D spausdinimas ir kompiuterinė gamyba. Jis vaizduoja paviršių kaip mažų trikampių, vadinamų briaunomis, seriją, kur kiekvienas briaunas apibūdinamas statmena kryptimi ir trimis taškais, vaizduojančiais trikampio viršūnes. Programos naudoja gautus duomenis, kad nustatytų 3D formos, kurią turi sukurti gamintojas, skerspjūvį. STL failo formatu nėra informacijos apie spalvą, tekstūrą ar kitus įprastus [CAD](/cad/) modelio atributus.

## Trumpa istorija ##

The development of STL file format dates back to 1987. Jį sukūrė 3D Systems, kad būtų galima naudoti komerciniuose 3D spausdintuvuose. 2009 m. buvo pasiūlyta atnaujinta STL failo formato versija, žinoma kaip STL 2.0, su failo formato atnaujinimais.

## Failo formato specifikacijos ##

STL failas vaizduoja paviršiaus geometriją naudojant briaunas. Briaunos apibrėžia 3D objekto paviršių ir yra vienareikšmiškai identifikuojamos vienetine normalia, kuri yra 1,0 ilgio trikampiui statmena linija, ir trimis viršūnėmis. Iš viso yra saugoma 12 skaičių kiekvienam aspektui kaip normalus ir kiekviena viršūnė nurodoma trimis koordinatėmis. StL faile nėra masto informacijos; koordinatės yra savavališkais vienetais.

STL failo formato specifikacijas galima išnagrinėti iš šių dviejų aspektų.

### Orientacija į aspektus ###

Faseto orientacija nustatoma pagal vieneto normalės kryptį ir viršūnių sąrašo tvarką. Aspektų orientacija nurodoma dviem būdais:

* Normalios krypties kryptis yra į išorę

* Viršūnės išvardytos prieš laikrodžio rodyklę iš išorės, laikantis dešinės rankos taisyklės.


### Viršūnės į viršūnę taisyklė ###

Pagal šią taisyklę kiekvienas trikampis turi dvi viršūnes su kiekvienu gretimu trikampiu. Taigi vieno trikampio viršūnė negali būti kito trikampio kraštinėje.

## Failų formatai ##

STL galimas ASCII ir dvejetainiu formatu kompaktiškam failo formatui.

### STL ASCII formatas ###

STL failo formato ASCII versija parašyta paprastu ASCII. Tačiau dėl didelio dydžio failo formatas nepasirinktas kaip pageidaujamas naudoti formatas. ASCII STL failo sintaksė yra tokia:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. **normalios briaunos** koordinatė gali turėti priešakinį minuso ženklą; **viršūnės** koordinatės negali būti.

### STL dvejetainis formatas ###

Dvejetainis formatas naudoja sveikąjį IEEE skaičių ir slankiojo kablelio skaitinį vaizdą. Failo formatas pavaizduotas taip:

|Laukas|Informacija|
---|---|
|Antraštė|80 simbolių|
|Trikampių skaičius|4 baitų mažasis endianas be ženklo sveikasis skaičius|
|Kiekvieno trikampio duomenys|12 32 bitų slankiojo kablelio skaičių|

Toliau pateiktas išsamesnis failo formato vaizdas.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Nuorodos Nr.

* [STL formatas] (http://www.fabbers.com/tech/STL_Format)

* [STL – pateikė Vikipedija](https://en.wikipedia.org/wiki/STL_(file_format))


