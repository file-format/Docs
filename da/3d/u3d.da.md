{
  "date": "2019-10-11",
  "keywords": [
"u3d fil",
"u3d filformat",
"hvad er en u3d fil",
"fil",
"u3d eksempel",
"u3d filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D - Universal 3D filformat",
  "description": "Lær om U3D-filformater og API'er, der kan åbne og oprette U3D-filer.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-dad"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en U3D fil?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/)-dokumenter understøtter indlejring af U3D-objekter og kan ses i Adobe Reader (version 7 og frem).

U3D-formatet blev udviklet med henblik på at etablere en universel standard for tredimensionel datalagring og -udveksling. Formatet finder dog sin primære anvendelse i kodning til 3D PDF i stedet for at blive brugt som et udvekslingsformat. Acrobat 3D konverterer en understøttet 3D-filtype til enten U3D eller PRC ved konvertering til PDF.

## U3D filformat

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

Den første udgave af U3D var fokuseret på de vigtigste repræsentationer af 3D-grafiske egenskaber såsom geometri, farve, teksturer, belysning, knogler og transformationsbaseret animation. Den anden og tredje udgave korrigerede nogle fejl i den første udgave, hvor tredje version er den mest almindeligt anvendte type i industrisoftware. Den fjerde udgave giver definitioner for højere ordens primitiver (buede overflader). [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) er tilgængelige online til brugerreference på ECMA-webstedet.

### Datatyper i U3D-filer

Den binære fil vil indeholde følgende typer: U8, U16, U32, U64, I16, I32, F32, F64 og String.

 * U8 : Et 8 bit heltal uden fortegn
 * U16 : Et 16 bit heltal uden fortegn
 * U32 : Et 32 bit heltal uden fortegn
 * U64 : Et 64 bit heltal uden fortegn
 * I16 : Et fortegnet 16 bit heltal
 * F32: En IEEE enkelt præcisionsflyder.
 * F64: En IEEE dobbelt præcisionsflyder.
 * String: Strenge i en U3D-fil starter med et usigneret 16-bit heltal, der definerer den samlede længde af tegnene i strengen. Strenge behandles altid som store og små bogstaver.

## U3D filstruktur

En U3D-fil indeholder en sekvens af blokke. Der er 3 forskellige typer af en blok i hver U3D-fil.

 * Filoverskriftsblok
 * Erklæringsblok
 * Fortsættelsesblok

Indlæseren bestemmer slutningen af en blok, hvis dataene i den blok ikke er påkrævet, eller hvis en dekoder for den bloktype ikke er tilgængelig.

{{< figure src="../u3d.png" alt="U3D filformat" >}}

### Filoverskriftsblok
En filoverskriftsblok indeholder filoplysninger, der bruges af den indlæste til at bestemme, hvordan filen skal læses.

### Erklæringsblok

Deklarationsblokkene indeholder information om objekterne i filen. Objekterne i en deklarationsblok skal defineres.

### Fortsættelsesblok

Yderligere oplysninger om objekter erklæret i en erklæringsblok er angivet i fortsættelsesblokken. Hver fortsættelsesblok skal være tilknyttet en erklæringsblok.


## Referencer ##

* [U3D-filformat - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D filformatspecifikationer](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


