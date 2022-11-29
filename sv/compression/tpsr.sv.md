{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR File Format - TeamViewer Pilot Session Report File",
  "description":"Läs mer om TPSR-filformat och API:er som kan skapa och öppna TPSR-filer.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Vad är TPSR fil?

En TPSR är en anslutningsprotokollfil som används av TeamViewer Assist AR (tidigare känd som TeamViewer Pilot). Information som lagras i en TPSR-fil lagras i komprimerat [ZIP](/sv/compression/zip/) filformat. TPSR innehåller detaljerad historik över TeamViewer-anslutningar mellan en expert och en tekniker för att lösa problem och granskningsändamål. Information som finns i en TPSR-fil inkluderar enhetstyp, namn, Assist AR ID, Expert ID, datum och tid och anslutningens varaktighet. Dessa data lagras i en [JSON](/sv/web/json/)-fil i det komprimerade TPSR-arkivet.

## TPSR filformat

En TPSR-fil lagras på skiva i ZIP-arkivfilformat där innehållet lagras i en JSON-fil. Den genereras automatiskt efter att Assist AR-anslutningen har slutförts förutsatt att alternativet Anslutningsrapportering är aktiverat i TeamViewer.

TeamViewer Assist AR låter experter ansluta till tekniker för att få LIVE-flöde från fjärränden via mobilkameran. De kan hjälpa teknikerna att lösa problemet via telefon.

## Öppna TPSR-filer

Du kan öppna TPSR-filer med skrivbordsversionen av TeamViewer-programvaran. Om den är installerad på din compture, dubbelklickar du på TPSR-filen för att öppna den i TeamViewer-programvaran. TPSR-filer kan också exporteras till [PDF](/sv/pdf/)-filer eller kan skrivas ut för att få en utskriven kopia av protokollfilen.

## Referenser ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

