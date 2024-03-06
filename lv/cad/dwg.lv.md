{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Faila formāts",
"CAD",
"Atvērt",
"Izveidot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DWG faila formātu un API, kas var izveidot un atvērt DWG failus.",
  "title": "DWG faila formāts",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DWG fails?

Faili ar DWG paplašinājumu ir patentēti bināri faili, kas tiek izmantoti 2D un 3D dizaina datu saturēšanai. Tāpat kā DXF, kas ir ASCII faili, DWG ir binārais faila formāts CAD (Computer Aided Design) zīmējumiem. Tas satur vektora attēlu un metadatus CAD failu satura attēlošanai. DWG failu skatīšanai operētājsistēmā Windows ir pieejami bezmaksas skatītāji, piemēram, Autodesk bezmaksas DWG TrueView. Ir arī citas trešo pušu lietojumprogrammas, kas atbalsta DWG failu sasniegšanu. DWG faili satur lietotāja izveidotu informāciju un ietver:

* Dizaini

* Ģeometriskie dati

* Kartes un fotogrāfijas


Šo formātu plaši izmanto arhitekti, inženieri un dizaineri dažādiem projektēšanas mērķiem.

## Īsa vēsture ##

DWG file format has evolved with the time since its formal introduction in 1982. Īss pagātnes notikumu pārskats no vēstures viedokļa ir šāds.

**1982. gads:** Autodesk licencēja DWG faila formātu , kuru 1970. gadā izstrādāja Maiks Ridls kā AutoCAD pamatu.

**1998. gads:** Izlaižot AutoCAD R14.01, Autodesk pievienoja failu verifikāciju, izmantojot funkciju DWGCHECK, kas programmas izveidotajos DWG failos ievietoja šifrētu kontrolsummu un produkta kodu, ko Autodesk sauc par WaterMark.

**2006:** Autodesk modificēja AutoCAD 2007, lai iekļautu TrustedDWG tehnoloģiju, lai DWG failos iegultu teksta virkni Autodesk DWG. Šis fails ir uzticams DWG, kuru pēdējo reizi saglabāja Autodesk lietojumprogramma vai Autodesk licencēta lietojumprogramma. Tā mērķis bija palīdzēt Autodesk programmatūras lietotājiem nodrošināt, ka šie faili ir izveidoti ar Autodesk vai RealDWG lietojumprogrammu, kam noteikti vajadzētu palīdzēt samazināt nesaderības risku.

## Faila struktūra ##

DWG ir bijis viens no plaši izmantotajiem failu formātiem dažādās lietojumprogrammās, un tam ir spēcīga failu struktūra. Tā kā DWG ir binārais faila formāts, tas nav cilvēkiem lasāms kā vienkāršs ASCII [DXF](/cad/dxf/) faila formāts. DWG faili parasti ietver informāciju par attēla koordinātām un visiem ar to saistītajiem metadatiem. OpenDesign lejupielādei ir pieejami pilni [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) DWG faila formāti. DWG faila formāta failu struktūra ir apkopota šādi.

**Galvene**: faila galvene sastāv no DWG galvenes mainīgajiem un informācijas par cikliskās redundances pārbaudi (CRC), ko izmanto kļūdu noteikšanai. Katra apakšiedaļa ir specializēts vektors, kurā tiek izmantoti dažāda garuma biti, lai attēlotu dažādas etiķetes. Piemēram, pirmie 6 DWG galvenes mainīgā biti apzīmē versijas virkni.

**Klases definīcijas:** DWG failā var būt vairākas klases atkarībā no konkrētā .dwg faila mērķa. Papildus citai informācijai, piemēram, klases metadatu lielums klases datu apgabalā, klases numurs un kontrolsumma.

**Veidne**: šī nav obligāta, un R15 un R15 versijām šī sadaļa atrodas zem sadaļas Brīvā vieta.

**Papildinājums**: metadati tiek papildināti ar sufiksu un pēcfiksāciju ar noteiktu baitu skaitu, kas padara vecākās AutoCAD programmatūras versijas pārsūtīšanas saderīgas ar jauno DWG faila formātu.

**Attēla dati**: šīs sadaļas metadati ir atkarīgi no konkrētā .dwg veida. R14 un R15 lietotājiem šī sadaļa nav obligāta.

**Objektu dati**: objekta dati sastāv no pilna tabulas entītiju saraksta, vārdnīcas ierakstiem utt., kas atbilst esošajam objektu sarakstam.

**Objektu karte**: katra objekta atrašanās vieta failā ir norādīta šajā faila sadaļā. Lielākā daļa metadatu šajā sadaļā ir failu rokturi, kuriem ir nozīme objekta identificēšanā un atkārtotā atveidē.

**Objektu brīvā vieta**: šī sadaļa nav obligāta visiem lietotājiem

**Otrā galvene**: faila galvenes sadaļas dublikāts DWG faila beigās

## Atsauces Nr.

* [DWG faila formāta specifikācijas](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [DWG faila specifikācija](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG — Wikipedia](https://en.wikipedia.org/wiki/.dwg)


