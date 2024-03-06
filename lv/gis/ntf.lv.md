{
  "date": "2021-07-28",
  "keywords": [
"ntf failu",
"ntf faila formātā",
"kas ir ntf fails",
"failu",
"ntf piemērs",
"ntf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF — nacionālā pārsūtīšanas formāta faili",
  "description": "Uzziniet par NTF failu formātu un API, kas var izveidot un atvērt NTF failus.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-lvf"
}
},
  "lastmod": "2021-07-28"
}

## Kas ir NTF fails?
Failus ar paplašinājumu .ntf sauc par **Nacionālo pārsūtīšanas formātu (NTF)** failiem; galvenokārt izmanto Apvienotās Karalistes Ordnance Survey (OS); īpaši ģeotelpisko datu pārsūtīšanai. To pārvalda Lielbritānijas Standartu institūcija. Tas ir kļuvis par standarta pārsūtīšanas formātu Ordnance Survey digitālajiem datiem. Apvienotās Karalistes Nacionālā režģa projekcija, kas ir šķērsvirziena Mercator veids, satur visu NTF failu ģeogrāfisko atsauci.

## NTF faila formāts
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Šis faila formāts tika ieviests, lai novērstu **PCIDSK** vektora segmenta ierobežojumu, kuram katrā struktūrā ir tikai viens atribūta lauks, taču ir daudz dažādu atribūtu, kurus var iegūt ar vektordatiem. Lai apietu, NTF faila formātā ir divi segmenti. Katrs segments sastāv no vieniem un tiem pašiem vektoriem, bet ar dažādiem atribūtiem. Pirmajā NTF vektora faila segmentā ir vektori ar objekta koda numuru kā atribūtu. Otrajā segmentā ir vektori ar vērtību kā atribūtu.

### Koordinātu atsauces sistēma
GDB bibliotēka attēlo rastra un vektora datus ar atbilstošiem TM projekcijas parametriem:

- Atsauces garums: 49,0
- Atsauces platums: 2.0
- Viltus Easting: 400 000
- Viltus ziemeļu virziens: -100 000
- Mērogs: 0,9996012717
- Elipsoīds: Airy 1830 (E009)
Nav pieejams atbalsts NTF failu atjaunināšanai vai rakstīšanai, kā arī DTM failus nevar saistīt.

### Ogrinfo piemērs
Nākamajā piemērā NTF failā tiek izmantots **ogrinfo**, lai izgūtu slāņu numurus:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Atsauces

* [AK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Tīmekļa kartēšana — ilustrējis Tailers Mičels](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


