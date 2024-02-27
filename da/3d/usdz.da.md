{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"usdz fil",
"usdz filformat",
"filformat",
"3d",
"Usdz fil download"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ - Universal Scene Beskrivelse ZIP Format",
  "description": "Lær om USDZ filformat og API'er, der kan åbne og oprette USDZ filer.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-daz"
}
},
  "lastmod": "2021-02-01"
}

## Hvad er en USDZ fil?

En fil med .usdz er et ukomprimeret og ukrypteret ZIP-arkiv til filformatet [USD](/3d/usd/) (Universal Scene Description), der indeholder og proxyer for filer i andre formater (såsom teksturer og animationer), der er indlejret i arkivet og kører dem direkte med USD-løbetiden uden behov for udpakning. USDZ-filer er pakker, hvis design er baseret på den nye abstraktion på Ar-niveau af en pakke. Usdz blev registreret hos IANA og har medietypenavnet på modellen og et undertypenavn på vnd.usd+zip, og dets detaljer kan findes som på [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ filformat

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP-begrænsninger

USDZ-filformatet bruger ZIP-filformatet uden nogen komprimering og kryptering. Dette var designet til at opfylde to krav:

 * For en pakke, der allerede er indlæst i hukommelsen eller som en enkelt fil på disken, er API'erne tilgængelige i USD for at få adgang til dataene i billedet
 * Der skulle ikke være behov for at udpakke filer til disk eller tildele mere heap-lagerplads

Med USDZ er begge disse krav opfyldt, da de fleste billedformater i sig selv tillader interne komprimeringsordninger, hvilket resulterer i en kompakt filstørrelse.

### Layoutkrav

USDZ-pakker kræver, at layoutet af filer i pakken er, at dataene for hver fil skal begynde med et multiplum af 64 bytes fra begyndelsen af pakken. Pakken bør dog starte med en indbygget [USD](/3d/usd/)-fil i tilfælde af at målrette pakken med en simpel reference. I et sådant tilfælde omtales denne første USD-fil som standardlaget. Kunder, der ønsker at levere streambart indhold, ønsker måske også at overveje andre layout-begrænsninger.

## USDZ fil download
Da usdz-filerne er pakket med andre billeder af høj kvalitet og usd-filer, kan de optage større disklagerplads. Her kan du finde en enkel og mindre USDZ eksempelfil til download:

- [Sample.usdz](../sample.usdz)

## Referencer

* [USDZ filformatspecifikationer](https://openusd.org/release/spec_usdz.html)


