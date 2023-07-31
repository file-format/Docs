{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om ACCDT-filformat och API:er som kan skapa och öppna ACCDT-filer.",
  "title" :"ACCDT - Microsoft Access 2007 Template Database File Format",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Vad är en ACCDT fil?

En fil med filändelsen .accdt är en Microsoft Access-databasmallfil som innehåller fördefinierade databaselement. Dessa element är en samling strukturer som definierar en databasapplikationer såsom databasscheman för lagring av data, layoutbeskrivning för vyer av data och metadata som beskriver databasen. Eftersom de är mallfiler kan ACCDT-filer användas för att skapa databaser baserat på mallinställningarna som finns tillgängliga i dessa. Resulterande databasfiler sparas som [ACCDB](/sv/database/accdb/)-filer och fylls i med data i tabeller. Microsoft Access 2007 och framåt kan öppna ACCDT-filer.

## ACCDT filformat

ACCDT-mallfiler är baserade på Office Open XML-specifikationerna och all data finns i ett ZIP-paket. Databasens struktur och innehållsinformation finns i [XML](/sv/web/xml/)-filer och textfiler och länkade till varandra via relationer. Du kan byta namn på en ACCDT-fil till tillägget [.zip](/sv/compression/zip/) och använda valfri komprimeringsprogramvara för att extrahera innehållet i ZIP-arkivet.

### Filstruktur

ACCDT-filer är paket som innehåller en samling relaterade delar. Varje **del** lagrar information om innehållet i en databasapplikation som använder XML, text och binära format, som inkluderar:

* Databasobjekt
* Tillhörande metadata
* Paketets struktur

#### Paket

Ett paket är ett [ZIP](/sv/compression/zip/)-arkiv som innehåller flera delar och överensstämmer med de öppna förpackningskonventionerna som anges i [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT-filer måste innehålla minst en Template metadaa-del som bör vara målet för en relation. Denna mallmetadata är startdelen av en ACCDT-fil.

#### Del

En del är en ström av bytes som har en tillhörande typ för att specificera arten och typen av innehåll som lagras i den. Delaruppräkning anger giltiga delar, giltiga innehållstyper och obligatoriska relationer mellan alla delar i ett paket.

#### Förhållande

"Paketrelation" - där målet är en del och källan är paketet som helhet.

`Part-to-Part Relationship` - där målet är en del och källan är en del i paketet.

`Explicit relation` - där en resurs refereras från innehållet i en källdel genom att referera till ett relationselement med värdet på dess ID-attribut.

`Implicit relation` - ett förhållande som inte är explicit.

`Intern relation` - där målet är en del av paketet.

`Extern relation` - där målet är en extern resurs som inte finns i paketet.

## Referenser ##

* [Åtkomstmallfilformat](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

