{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file DDS - File immagine superficie DirectDraw",
  "description":"Scopri il formato di file DDS e le API che possono creare e aprire file DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Che cos'è un file DDS?

Un file DDS è un file di immagine raster che utilizza il formato contenitore DirectDraw Surface (DDS). Memorizza trame non compresse e compresse (DXTn) e implementa diversi tipi per memorizzare diversi tipi di dati. Supporta anche diversi tipi di dati come trame a strato singolo, trame con mipmap, mappe di cubi, mappe di volume e matrici di texture. Ciò consente ai file DDS di archiviare modelli di unità di texture per videogiochi oltre a foto digitali e sfondi desktop di Windows. Il formato file DDS è stato sviluppato da Microsoft per essere utilizzato con DirectX SDK.

## Formato file DDS

I file DDS vengono salvati come file binari e possono essere utilizzati con DirectX SDK. Utilizza la potenza di DirectX per sviluppare applicazioni di rendering in tempo reale come i giochi 3D.

### Layout del file DDS

Il [layout file DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) è stato documentato in dettaglio da Microsoft. Un file DDS binario contiene le seguenti informazioni.

* Una DWORD (numero magico) contenente il valore del codice a quattro caratteri 'DDS' (0x20534444).
* Una descrizione dei dati nel file.

DDS_HEADER descrive i dati e DDS_PIXELFORMAT descrive il formato pixel. Entrambi sostituiscono le deprecate strutture DDSURFACEDESC2, DDSCAPS2 e DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

La [guida alla programmazione del formato di file DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) elabora ulteriormente i dettagli tecnici di questo formato di file.

## Riferimenti

* [DDS - Di Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
