{
  "date" : "2021-07-28",
  "keywords" :[ "soubor ntf", "formát souboru ntf", "co je soubor ntf", "soubor", "příklad ntf", "přípona souboru ntf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - National Transfer Format Files",
  "description":"Další informace o formátu souborů NTF a rozhraních API, která mohou vytvářet a otevírat soubory NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Co je soubor NTF?
Soubory s příponou .ntf se nazývají soubory **National Transfer Format (NTF)**; většinou používán britským Ordnance Survey (OS); speciálně pro přenos geoprostorových dat. Je řízena British Standards Institution. Stal se standardním přenosovým formátem pro digitální data Ordnance Survey. Britská projekce National Grid, což je typ Transverse Mercator, obsahuje všechny georeferenční informace pro soubory NTF.

## Formát souboru NTF
Formát souboru NTF je ve vlastnictví Ordnance Survey ve Spojeném království; podporované knihovnou GDB pro import. Současná verze formátu souboru NTF je 2.0. Tento formát souboru byl zaveden s cílem vyřešit omezení vektorového segmentu **PCIDSK**, který má pouze jedno pole atributu na strukturu, ale existuje celá řada atributů, které lze extrahovat vektorovými daty. Chcete-li obejít formát souboru NTF, je tvořen dvěma segmenty. Každý segment se skládá ze stejných vektorů, ale s různými atributy. První segment vektorového souboru NTF obsahuje vektory s číslem kódu prvku jako atributem. Druhý segment obsahuje vektory s hodnotou jako atributem.

### Souřadnicový referenční systém
Knihovna GDB představuje rastrová a vektorová data s vhodnými charakteristikami projekce TM:

- Referenční zeměpisná délka: 49,0
- Referenční zeměpisná šířka: 2,0
- Falešný východ: 400 000
- Falešné severování: -100 000
- Měřítko: 0,9996012717
- Ellipsoid: Airy 1830 (E009)
Není k dispozici žádná podpora pro aktualizaci nebo zápis souborů NTF, ani nelze propojit soubory DTM.

### Příklad Ogrinfo
Následující příklad používá **ogrinfo** v souboru NTF k načtení čísel vrstev:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Reference

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Webové mapování – ilustroval Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

