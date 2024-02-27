{
  "date": "2019-12-09",
  "keywords": [
"3mf fil",
"3mf filformat",
"hvad er en 3mf fil",
"fil",
"3mf eksempel",
"3mf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "Lær om 3MF filformat og API'er, der kan åbne og oprette 3MF filer.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-daf"
}
},
  "lastmod": "2019-12-09"
}

## Hvad er en 3MF fil?

3MF, 3D Manufacturing Format, bruges af applikationer til at gengive 3D objektmodeller til en række andre applikationer, platforme, tjenester og printere. Det blev bygget til at undgå begrænsningerne og problemerne i andre 3D-filformater, såsom [STL](/cad/stl/), til at arbejde med de nyeste versioner af 3D-printere. 3MF er et relativt nyt filformat, der er udviklet og udgivet af 3MF-konsortiet. Den er rig nok til fuldt ud at beskrive en model, idet den bevarer intern information, farve og andre egenskaber, der gør den udbyggelig til at understøtte nye innovationer inden for 3D-print. Formatet er udvideligt, i stand til at blive bredt vedtaget og fri for problemer, der rammer andre udbredte filformater.

## Kort historie om 3MF filformat

De eksisterende begrænsninger i tilgængelige modelbeskrivende filformater, såsom STL og andre, fører til, at de førende mærker går sammen og formulerer et mere udvidelsesvenligt filformat til 3D-print. En vigtig overvejelse var, hvordan applikationer skulle videregive modeldata til 3D-printere. 3MF-konsortiet blev derfor til for at bakke op om et nyt 3D-filformat kaldet 3MF med det formål at gøre det udvideligt nok til at imødekomme behovene for 3D-print. Flere virksomheder var en del af dette konsortium, herunder Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP og andre. Microsoft donerede sit igangværende 3D-filformat som udgangspunkt for 3MF-konsortiets fælles videreudvikling af specifikationen.

## 3MF filformat - flere oplysninger

3MF er et XML-baseret dataformat – menneskelæselig komprimeret XML – der inkluderer definitioner af data relateret til 3D-fremstilling, herunder tredjeparts udvidelsesmuligheder for brugerdefinerede data. 3MF-filformatet blev designet med tanke på de begrænsninger og problemer, som andre 3D-filformater står over for. Dette førte til formuleringen af 3MF filformat, der er:

* **Fuldstændig:** Indeholder alle nødvendige model-, materiale- og ejendomsoplysninger i et enkelt arkiv

* **Læsbar for mennesker:** Bruger almindelige strukturer såsom OPC, [ZIP](/compression/zip/) og XML for at lette udviklingen

* **Simpelt:** En kort, klar specifikation, der gør udviklingen nem og valideringen hurtig

* **Udvidelig:** Udnyttelse af XML-navneområder giver mulighed for både offentlige og private udvidelser, samtidig med at kompatibiliteten bevares

* **Utvetydigt:** Tydelige sprog- og overensstemmelsestest sikrer, at en fil altid er konsistent fra digital til fysisk

* **Gratis:** Adgang til og implementering af 3MF-specifikationen er og vil altid være fri for royalties, patenter og licenser


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF filformatspecifikationer

3MF-filformatet bruger Open Packaging-specifikationerne i form af ZIP-arkiv til sin fysiske model. Det inkluderer et veldefineret sæt af dele og relationer, der opfylder et bestemt formål i dokumentet. Dette gør også, at formatet følger pakkefunktionen inklusive digitale signaturer og miniaturebilleder.

### 3MF-dokumentet - en oversigt

Et typisk 3MF-dokument ser ud som følger:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Navn**|**Beskrivelse**|**Selationskilde**|**Påkrævet/Valgfri**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Kerneegenskaber|OPC-delen, der indeholder forskellige dokumentegenskaber.|Pakke|VALGFRI
|Digital Signature Origin|OPC-delen, der er roden til digitale signaturer i pakken.|Pakke|VALGFRI
|Digital signatur|OPC-dele, der hver indeholder en digital signatur.|Digital signaturoprindelse|VALGFRI
|Digital signaturcertifikat|OPC-dele, der indeholder et digitalt signaturcertifikat.|Digital signatur|VALGFRI
|PrintTicket|Indeholder indstillinger, der skal bruges ved output af 3D-objekt(er) i 3D-modeldelen.|3D-model|VALGFRI
|Thumbnail|Indeholder et lille JPEG- eller PNG-billede, der repræsenterer 3D-objekterne i pakken eller pakken som helhed.|Pakke|VALGFRI
|3D-tekstur|Indeholder en tekstur, der bruges til at anvende farve på et 3D-objekt i 3D-modeldelen (tilgængelig for udvidelser)|3D-model|VALGFRI
|Tilpassede dele|OPC-dele, der er forbundet med metadata|Pakke|VALGFRI

Sektionerne [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) og [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) i specifikationsdokumentet giver detaljerede oplysninger om 3MF-dokumentet.

## Referencer ##

* [3MF filformatspecifikationer](https://github.com/3MFConsortium/spec_core)

* [3MF - Af Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


