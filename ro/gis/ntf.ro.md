{
  "date" : "2021-07-28",
  "keywords" :[ "fișier ntf", "format fișier ntf", "ce este un fișier ntf", "fișier", "exemplu ntf", "extensie fișier ntf", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF – fișiere în format de transfer național",
  "description":"Aflați despre formatul de fișier NTF și despre API-urile care pot crea și deschide fișiere NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Ce este un fișier NTF?
Fișierele cu extensia .ntf sunt numite fișiere **National Transfer Format (NTF)**; utilizat în cea mai mare parte de către UK Ordnance Survey (OS); special pentru transferul de date geospațiale. Este gestionat de British Standards Institution. A devenit formatul standard de transfer pentru datele digitale Ordnance Survey. Proiecția National Grid din Marea Britanie, care este un tip de Mercator transversal, deține toate informațiile georeferențiate pentru fișierele NTF.

## Format de fișier NTF
Formatul de fișier NTF este deținut de Ordnance Survey din Regatul Unit; suportat de biblioteca GDB pentru import. Versiunea actuală a formatului de fișier NTF este 2.0. Acest format de fișier a fost introdus pentru a aborda o limitare a segmentului vectorial **PCIDSK** care are un singur câmp de atribut per structură, dar există o varietate de atribute care pot fi extrase cu date vectoriale. Pentru a ocoli formatul de fișier NTF este constituit ca având două segmente. Fiecare segment este format din aceiași vectori, dar cu atribute diferite. Primul Segment al unui fișier vectorial NTF conține vectorii cu numărul de cod al caracteristicii ca atribut. Al doilea segment conține vectorii cu valoarea ca atribut.

### Sistem de referință de coordonate
Biblioteca GDB reprezintă date raster și vectoriale cu caracteristicile corespunzătoare de proiecție TM:

- Longitudine de referință: 49,0
- Latitudine de referință: 2.0
- Est fals: 400000
- Nord fals: -100000
- Scară: 0,9996012717
- Elipsoid: Airy 1830 (E009)
Nu este disponibil niciun suport pentru actualizarea sau scrierea fișierelor NTF și nici fișierele DTM nu pot fi legate.

### Ogrinfo exemplu
Următorul exemplu utilizează **ogrinfo** pe un fișier NTF pentru a prelua numerele stratului:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referințe

* [Format de transfer național al Regatului Unit (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Mapping Web - Ilustrat de Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

