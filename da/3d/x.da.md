{
  "date": "2020-01-11",
  "keywords": [
"x fil",
"x filformat",
"hvad er en x-fil",
"fil",
"x eksempel",
"x filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X - DirectX 2.0 filformat",
  "description": "Lær om DirectX X-filformat og API'er, der kan åbne og oprette DirectX X-filer.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--dax"
}
},
  "lastmod": "2020-01-11"
}

## Hvad er en X fil?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. Det blev brugt til 3D-grafikgengivelse i spil og specificerer strukturerne for masker, teksturer, animationer og brugerdefinerede objekter. Det har været forældet siden 2014, da Autodesk FBX-filformatet fungerer bedre som et mere moderne format. X er skabelondrevet og er fri for enhver brugsviden.

Du kan åbne DirectX X-filer ved hjælp af Microsoft DirectX og almindelige teksteditorer.

## X filformat

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) indeholder referenceoplysninger for de API-elementer, der bruges til at arbejde med DirectX .x-filer. Formatet giver dataprimitiver på lavt niveau, der bruges af andre applikationer til at definere primitiver på højere niveau gennem dataskabeloner. DirectX 6.0 introducerede grænseflader og metoder, der gør det muligt at læse fra og skrive til .x-filer. DirectX 3.0 introducerede en binær version af dette filformat.

[X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) defineret af DirectX 9 indeholder referenceoplysninger for .x-filer i binære såvel som tekstkodninger.

### Binær kodning

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definerer DirectX X-formatet som en tokeniseret repræsentation af tekstformatet. Disse tokens kan være selvstændige for at give grammatisk struktur eller kan være rekordbærende tokens, der leverer de nødvendige data.

#### Header

Den binære header kan læses og skrives ved hjælp af følgende definitioner.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Tekstkodning

DirectX .x-filer afhænger ikke af den måde, filen bruges på, og er ikke specifik for nogen applikation. Denne skabelondrevne tilgang tillader, at .x-filformatet kan bruges af enhver klientapplikation.


#### Header

Overskriften med variabel længde er obligatorisk og skal være i begyndelsen af datastrømmen. Overskriften indeholder følgende data.

|Type |Undertype |Størrelse |Indhold |Indholdsbetydning|
---|---|---|---|---|
|Magisk nummer (påkrævet)| | 4 bytes |xof |
|Versionsnummer (påkrævet) |Stornummer |2 bytes |03 |Storversion 3|
| |Minortal |2 bytes |02 |Minorversion 2|
|Formattype (påkrævet)| |4 bytes |txt  |Tekstfil|
| | | |bin| Binær fil|
| | | |tzip| MSZip komprimeret tekstfil|
| | | |bzip| MSZip komprimeret binær fil|
|Floatstørrelse (påkrævet)| |4 bytes| 0064| 64-bit flydere|
| | | |0032 |32-bit flydere|


## Referencer

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9-filformatreference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

