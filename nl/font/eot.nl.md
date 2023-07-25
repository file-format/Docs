{
  "date" : "2020-08-20",
  "keywords" :[ "eot-bestand", "eot-bestandsindeling", "wat is een eot-bestand", "bestand", "eot-voorbeeld", "eot-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType-lettertypebestandsindeling",
  "description":"Meer informatie over EOT-bestandsindeling en API's om EOT-bestanden te maken en te openen.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Wat is een EOT-bestand?

Een bestand met de extensie .eot is een OpenType-lettertype dat is ingesloten in een document. Deze worden meestal gebruikt in webbestanden zoals een webpagina. Het is gemaakt door Microsoft en wordt ondersteund door Microsoft-producten, inclusief het PowerPoint-presentatiebestand [.pps](/nl/presentation/pps). Het bestand is niet van primair gebruik en is een soort begeleidend document bij het hoofddocument of de webpagina. Net als bij OTF-lettertypen ondersteunt EOT zowel Postscript- als TrueType-contouren voor de glyphs. EOT-bestanden zijn kleiner omdat ze zijn gecomprimeerd met LZ-compressie. EOT gebruikt een Microsoft-tool om een lettertype te maken van bestaande TTF/OTF-lettertypen.

## Korte geschiedenis

Het EOT-lettertype werd in 2007 ingediend bij W3C als onderdeel van CSS3, maar vanwege de vereisten om permanent op een extern systeem te worden geïnstalleerd, werd het de reden van afwijzing. Het werd in maart 2008 opnieuw ingediend, maar W3C koos uiteindelijk voor [Web Font Format](/nl/font/woff/) (WOFF), dat toen gestandaardiseerd was.

## EOT-bestandsindeling

Details van EOT-bestandsindelingen zijn te vinden op [W3-inzendingspagina](https://www.w3.org/Submission/EOT/#FileFormat) en werken de structuur uit die door deze lettertype-indeling wordt gebruikt. De EOT bestaat uit een enkele EMBEDDEDFONT-structuur die voldoende basisinformatie biedt over de naam van het lettertype en de ondersteunde tekens. Door deze informatie in te pakken, kunnen User Agents voorkomen dat het lettertype wordt uitgepakt, gedecomprimeerd of geïnstalleerd als het al op de computer aanwezig is.

### EMBEDDEDFONT-structuur
De EMBEDDEDFONT-structuur heeft drie revisies ondergaan, met toevoeging van aanvullende gegevens aan het einde van de structuur bij elke revisie. De laatste revisie van de EMBEDDEDFONT-structuur is zoals hieronder weergegeven.

|Gegevenstype|Invoernaam|Beschrijving|
---|---|---|
|unsigned long|EOTSize|Totale lengte van de structuur in bytes (inclusief string- en lettertypegegevens)|
|unsigned long|FontDataSize|Lengte van het OpenType-lettertype (FontData) in bytes|
|unsigned long|Versie|Versienummer van dit formaat - 0x00020002|
|unsigned long|Vlaggen|Verwerkingsvlaggen|
|byte[10]|FontPANOSE|De PANOSE-waarde voor dit lettertype - zie http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|In Windows is dit afgeleid van TEXTMETRIC.tmCharSet. Deze waarde geeft de tekenset van het lettertype aan. DEFAULT_CHARSET (0x01) geeft geen voorkeur aan. - Zie https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Als de bit voor ITALIC is ingesteld in OS/2.fsSelection, is de waarde 0x01 - Zie http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|De gewichtswaarde voor dit lettertype - zie http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Typ vlaggen die informatie geven over insluitrechten - zie http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Magisch nummer voor EOT-bestand - 0x504C. Wordt gebruikt om te controleren op gegevenscorruptie.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - Zie http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Zie http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - Zie http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - Zie http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - Zie http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63) - Zie http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Zie https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Gereserveerd1|Gereserveerd - moet 0 zijn|
|unsigned long|Gereserveerd2|Gereserveerd - moet 0 zijn|
|unsigned long|Gereserveerd3|Gereserveerd - moet 0 zijn|
|unsigned long|Gereserveerd4|Gereserveerd - moet 0 zijn|
|unsigned short|Opvulling1|Opvulling om een lange uitlijning te behouden. Opvulwaarde moet altijd worden ingesteld op 0x0000.|
|unsigned short|FamilyNameSize|Aantal bytes gebruikt door de FamilyName-array|
|byte|FamilyName[FamilyNameSize]|Array van UTF-16 tekens met de lengte van FamilyNameSize-bytes. Dit is de Engelstalige Font Family-string die te vinden is in de naamtabel van het lettertype (naam-ID = 1) - Zie https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Opvulling2|Opvulwaarde moet altijd op 0x0000 staan.|
|unsigned short|StyleNameSize|Aantal bytes gebruikt door de StyleName|
|byte|StyleName[StyleNameSize]|Array van UTF-16 tekens met de lengte van StyleNameSize-bytes. Dit is de Engelstalige Lettertype-subfamiliereeks die te vinden is in de naamtabel van het lettertype (naam-ID = 2) - Zie https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Opvulling3|Opvulwaarde moet altijd worden ingesteld op 0x0000.|
|unsigned short|VersionNameSize|Aantal bytes gebruikt door VersionName|
|bytes|VersionName[VersionNameSize]|Array van UTF-16-tekens met de lengte van VersionNameSize-bytes. Dit is de Engelse versiereeks die te vinden is in de naamtabel van het lettertype (naam-ID = 5) - Zie https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Opvulwaarde moet altijd worden ingesteld op 0x0000.|
|unsigned short|FullNameSize|Aantal bytes gebruikt door FullName|
|byte|FullName[FullNameSize]|Array van UTF-16-tekens met de lengte van FullNameSize-bytes. Dit is de Engelse volledige naamreeks die te vinden is in de naamtabel van het lettertype (naam-ID = 4) - Zie https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Opvulling5|Opvulwaarde moet altijd worden ingesteld op 0x0000.|
|unsigned short|RootStringSize|Aantal bytes gebruikt door de RootString-array|
|byte|RootString[RootStringSize]|Array van UTF-16-tekens met de lengte van RootStringSize-bytes.|
|unsigned long|RootStringCheckSum|RootString CheckSum-waarde. Zie het algoritme om RootStringChecksum hieronder te verwerken.|
|unsigned long|EUDCCodePage|Codepage-waarde nodig voor EUDC-lettertypeondersteuning.|
|unsigned short|Opvulling6|Opvulwaarde moet altijd worden ingesteld op 0x0000.|
|unsigned short|SignatureSize|Aantal bytes dat door de Signature-array wordt gebruikt. Momenteel gereserveerd en moet worden ingesteld op 0x0000.|
|byte|Signature[SignatureSize]|Momenteel gereserveerd. Als de SignatureSize 0x0000 is, heeft deze array geen lengte.|
|unsigned long|EUDCFlags|Verwerkingsvlaggen voor het EUDC-lettertype. Typische waarden zijn mogelijk TTEMBED_XORENCRYPTDATA en TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Aantal bytes gebruikt door de Signature-array.|
|byte|EUDCFontData[EUDCFontSize]|Aantal bytes dat is gebruikt voor de EUDC-lettertypegegevens. Als de EUDCFontSize 0x00000000 is, heeft deze array geen lengte.|
|byte|FontData[FontDataSize]|De lettertypegegevens voor dit EOT-bestand. De gegevens kunnen worden gecomprimeerd of XOR-gecodeerd zoals aangegeven door de verwerkingsvlaggen.|

## Referenties

* [EOT-bestandsindeling](https://www.w3.org/Submission/EOT/)
* [Ingesloten OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Lettertype insluiten](https://en.wikipedia.org/wiki/Font_embedding)

