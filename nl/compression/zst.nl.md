{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST-bestand - Zstandaard gecomprimeerd bestandsformaat",
  "description":"Meer informatie over de ZST-bestandsindeling en API's waarmee ZST-bestanden kunnen worden gemaakt en geopend.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-nl",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Wat is een ZST-bestand?

Een ZST-bestand is een gecomprimeerd bestand dat is gegenereerd met het Zstandard (zstd) compressie-algoritme. Het is een gecomprimeerd bestand dat door het algoritme is gemaakt met verliesloze compressie. ZST-bestanden kunnen worden gebruikt om verschillende soorten bestanden te comprimeren, zoals databases, bestandssystemen, netwerken en games. De Z-standaard wordt beheerst door [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), waarin het algemene compressiemechanisme, het mediatype en de inhoudscodering worden beschreven.

## ZST-bestandsindeling

ZST-bestanden worden in gecomprimeerd bestandsformaat op schijf opgeslagen. Het compressiemechanisme is zoals beschreven door RFC 8878, dat RFC 8478 overbodig maakt.

## ZST-frames

Een ZST-bestand bestaat uit een of meer frames. Elk frame kan een Z-standaardframe of een frame zijn dat kan worden overgeslagen. Een Zstandard-frame bevat gecomprimeerde gegevens, terwijl een frame dat kan worden overgeslagen aangepaste gebruikersmetagegevens bevat.

### Zstandaard frame

Een Zstandaard frame heeft de volgende opbouw.

|Veld|Grootte in bytes|
---|---|
|Magisch nummer |4 bytes|
|Frame_Header |2-14 bytes|
|Gegevensblok |n bytes|
|[Meer gegevensblokken] ||
|[Content_Checksum] |4 bytes|

### Frame dat kan worden overgeslagen

Met een frame dat kan worden overgeslagen, kunnen door de gebruiker gedefinieerde metagegevens worden ingevoegd in een stroom van aaneengeschakelde frames. De structuur van een frame dat kan worden overgeslagen is als volgt.

|Magic_Number |Frame_Size |Gebruikersgegevens|
---|---|---|
|4 bytes |4 bytes |n bytes|

## Referenties ##

* [RFC 8878 Zstandaard-compressie](https://www.rfc-editor.org/rfc/rfc8878)


