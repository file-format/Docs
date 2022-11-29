{
  "date" : "2020-01-11",
  "keywords" :[ "x fil", "x filformat", "vad är en x-fil", "fil", "x exempel", "x filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 filformat",
  "description":"Lär dig om DirectX X-filformat och API:er som kan öppna och skapa DirectX X-filer.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Vad är X fil?

En fil med filtillägget .x hänvisar till [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics äldre filformat som introducerades med Microsoft DirectX 2.0. Den användes för 3D-grafikrendering i spel och specificerar strukturerna för maskor, texturer, animationer och användardefinierade objekt. Det har blivit utfasat sedan 2014 eftersom Autodesk FBX-filformatet fungerar bättre som ett modernare format. X är malldrivet och är fri från all användningskännedom.

Du kan öppna DirectX X-filer med Microsoft DirectX och vanliga textredigerare.

## X filformat

[X-filreferensen](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) innehåller referensinformation för API-elementen som används för att arbeta med DirectX .x-filer. Formatet tillhandahåller dataprimitiver på låg nivå som används av andra applikationer för att definiera primitiver på högre nivå genom datamallar. DirectX 6.0 introducerade gränssnitt och metoder som möjliggör läsning från och skrivning till .x-filer. DirectX 3.0 introducerade en binär version av detta filformat.

[X filformatreferens](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) som definieras av DirectX 9 innehåller referensinformation för .x filer i binära såväl som textkodningar.

### Binär kodning

Det [binära formatet](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definierar DirectX X-formatet som en tokeniserad representation av textformatet. Dessa tokens kan vara fristående för att ge grammatisk struktur eller kan vara rekordbärande tokens som tillhandahåller nödvändig data.

#### Rubrik

Den binära rubriken kan läsas och skrivas med hjälp av följande definitioner.

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

### Textkodning

DirectX .x-filer beror inte på hur filen används och är inte specifik för något program. Detta malldrivna tillvägagångssätt gör att .x-filformatet kan användas av alla klientprogram.


#### Rubrik

Rubriken med variabel längd är obligatorisk och måste finnas i början av dataströmmen. Rubriken innehåller följande data.

|Typ |Undertyp |Storlek |Innehåll |Innehåll Betydelse|
---|---|---|---|---|
|Magiskt nummer (obligatoriskt)| | 4 byte |xof |
|Versionsnummer (obligatoriskt) |Major Number |2 byte |03 |Major version 3|
| |Minor Number |2 bytes |02 |Minor version 2|
|Formattyp (obligatoriskt)| |4 byte |"txt " |Textfil|
| | | |"bin "| Binär fil|
| | | |"tzip"| MSZip komprimerad textfil|
| | | |"bzip"| MSZip komprimerad binär fil|
|Flytningsstorlek (obligatoriskt)| |4 byte| 0064| 64-bitars flyter|
| | | |0032 |32-bitars flyter|


## Referenser

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 File Format Reference](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

