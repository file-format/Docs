{
  "date": "2021-07-28",
  "keywords": [
"comhad ntf",
"Formáid comhaid ntf",
"Cad is comhad ntf ann",
"comhad",
"sampla ntf",
"Síneadh comhad ntf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF - Comhaid Formáide Aistrithe Náisiúnta",
  "description": "Foghlaim faoi fhormáid comhaid NTF agus APIs ar féidir leo comhaid NTF a chruthú agus a oscailt.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-gaf"
}
},
  "lastmod": "2021-07-28"
}

## Cad is comhad NTF ann?
Tugtar na Comhaid **Formáid Aistrithe Náisiúnta (NTF)** ar na comhaid a bhfuil síneadh .ntf acu; a úsáideann Suirbhéireacht Ordanáis na RA (OS) den chuid is mó; go sonrach le haghaidh aistriú sonraí geospásúla. Tá sé á bhainistiú ag an Institiúid um Chaighdeáin na Breataine. Is é an fhormáid aistrithe caighdeánach anois é do shonraí digiteacha na Suirbhéireachta Ordanáis. Coinníonn réamh-mheastachán Eangaí Náisiúnta na Ríochta Aontaithe, ar cineál Transverse Mercator é, an fhaisnéis ghearthagartha ar fad do chomhaid NTF.

## Formáid comhaid NTF
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Tugadh an fhormáid comhaid seo isteach chun aghaidh a thabhairt ar theorannú ar mhír veicteora **PCIDSK** nach bhfuil ach réimse tréithe amháin in aghaidh an struchtúir, ach tá tréithe éagsúla ann ar féidir a bhaint as sonraí veicteora. Chun dul timpeall ar an bhformáid comhaid NTF comhdhéanta mar dhá mhír. Tá gach deighleog comhdhéanta de na veicteoirí céanna, ach le tréithe éagsúla. Sa chéad Deighleog de chomhad veicteora NTF tá na veicteoirí a bhfuil an códuimhir gné mar an tréith. Sa dara mír tá na veicteoirí leis an luach mar an aitreabúid.

### Comhordaigh córas tagartha
Léiríonn an leabharlann GDB sonraí raster agus veicteoir leis na tréithe cuí teilgean TM:

- Domhanfhad Tagartha: 49.0
- Domhanleithead Tagartha: 2.0
- Oirir Bréagach: 400000
- Tuaisceart Bréagach: -100000
- Scála: 0.9996012717
- Ellipsoid: Airy 1830 (E009)
Níl aon tacaíocht ar fáil chun comhaid NTF a nuashonrú, nó a scríobh, agus ní féidir na comhaid DTM a nascadh leis.

### Ogriinfo shampla
Úsáideann an sampla seo a leanas **ogrinfo** ar chomhad NTF chun uimhreacha sraitheanna a fháil:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Tagairtí

* [Formáid Aistrithe Náisiúnta na Ríochta Aontaithe (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Mapáil Gréasáin - Léirithe ag Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


