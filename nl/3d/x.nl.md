{
  "date" : "2020-01-11",
  "keywords" :[ "x file", "x file format", "wat is een x file", "file", "x example", "x file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0-bestandsindeling",
  "description":"Meer informatie over de DirectX X-bestandsindeling en API's die DirectX X-bestanden kunnen openen en maken.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Wat is een X-bestand?

Een bestand met de extensie .x verwijst naar [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy-bestandsindeling die werd geïntroduceerd met Microsoft DirectX 2.0. Het werd gebruikt voor het renderen van 3D-graphics in games en specificeert de structuren voor meshes, texturen, animaties en door de gebruiker gedefinieerde objecten. Het is sinds 2014 verouderd omdat het Autodesk FBX-bestandsformaat beter dienst doet als een moderner formaat. X is sjabloongestuurd en is vrij van enige gebruikskennis.

U kunt DirectX X-bestanden openen met Microsoft DirectX en algemene teksteditors.

## X-bestandsindeling

De [X-bestandsreferentie](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) bevat referentie-informatie voor de API-elementen die worden gebruikt om werken met DirectX .x-bestanden. Het formaat biedt gegevensprimitieven op een laag niveau die door andere toepassingen worden gebruikt om primitieven op een hoger niveau te definiëren door middel van gegevenssjablonen. DirectX 6.0 introduceerde interfaces en methoden die het lezen van en schrijven naar .x-bestanden mogelijk maken. DirectX 3.0 heeft een binaire versie van dit bestandsformaat geïntroduceerd.

De [X-bestandsindelingsreferentie](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) gedefinieerd door DirectX 9 bevat referentie-informatie voor .x bestanden in zowel binair als tekstcoderingen.

### Binaire codering

Het [binaire formaat](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definieert het DirectX X-formaat als een tokenized representatie van het tekstformaat. Deze tokens kunnen op zichzelf staan om grammaticale structuur te geven of kunnen recorddragende tokens zijn die de nodige gegevens leveren.

#### Koptekst

De binaire header kan worden gelezen en geschreven met behulp van de volgende definities.

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

### Tekstcodering

DirectX .x-bestanden zijn niet afhankelijk van de manier waarop het bestand wordt gebruikt en zijn niet specifiek voor een toepassing. Dankzij deze sjabloongestuurde aanpak kan het .x-bestandsformaat door elke clienttoepassing worden gebruikt.


#### Koptekst

De koptekst met variabele lengte is verplicht en moet aan het begin van de gegevensstroom staan. De kop bevat de volgende gegevens.

|Type |Subtype |Grootte |Inhoud |Inhoud Betekenis|
---|---|---|---|---|
|Magisch nummer (vereist)| | 4 bytes |xof |
|Versienummer (verplicht) |Hoofdnummer |2 bytes |03 |Hoofdversie 3|
| |Minder getal |2 bytes |02 |Secundaire versie 2|
|Formaattype (vereist)| |4 bytes |"txt " |Tekstbestand|
| | | |"bak "| Binair bestand|
| | | |"zip"| MSZip gecomprimeerd tekstbestand|
| | | |"bzip"| MSZip gecomprimeerd binair bestand|
|Float maat (verplicht)| |4 bytes| 0064| 64-bits zweeft|
| | | |0032 |32-bits zweeft|


## Referenties

* [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9-bestandsindelingreferentie](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

