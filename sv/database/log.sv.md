{
  "date" : "2021-06-14",
  "keywords" :[ "LOG", "tillägg", "loggfil", "loggfilformat", "Databasfiltyp", "Databasfilformat", "vad är en loggfil" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om LOG-filformat och API:er som kan skapa och öppna LOG-filer.",
  "title" :"LOGG - Log File Format",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Vad är en LOG-fil?
En fil med filtillägget .log innehåller listan över vanlig text med tidsstämpel. Vanligtvis loggas vissa aktivitetsdetaljer av programvaran eller operativsystemen för att hjälpa utvecklarna eller användarna att spåra vad som hände vid en viss tidsperiod. Användare kan redigera dessa filer mycket enkelt genom att använda valfri textredigerare. Vanligtvis loggas felrapporterna eller inloggningsaktiviteterna av operativsystemen, men andra programvaror eller webbservrar genererar också loggfiler för att spåra besökare och för att övervaka bandbreddsanvändning.

## LOG Filformat
Filformatet LOG registrerar de typiska händelser som inträffar antingen i ett operativsystem, meddelanden mellan olika användare av en kommunikationsprogramvara eller någon annan programvara som körs. Vi kan helt enkelt säga att vissa meddelanden vid vissa tidsstämplar loggas i en LOG-fil. Några vanliga termer för loggning är:
### Händelseloggar
Den registrerar händelser som inträffar under körningen av ett system för att spåra och förstå systemets aktivitet och för att diagnostisera problem. De är viktiga för att identifiera aktiviteterna i komplexa system, vanligtvis när det gäller applikationer med mycket lite användarinteraktion.
### Transaktionsloggar
Nästan alla databassystem upprätthåller transaktionsloggen, som vanligtvis inte är avsedda som ett granskningsspår för senare analys, och som inte är läsbara för människor. Dessa loggar sparar bara ändringar av befintliga data för att göra det möjligt för databasen att återhämta sig från krascher eller andra datafel och hålla data i ett konsekvent tillstånd. Därför har databassystem vanligtvis både allmänna händelseloggar och transaktionsloggar.
### Meddelandeloggar
Textkommunikationen som sparas av Internet Relay Chat (IRC), program för snabbmeddelanden (IM), peer-to-peer fildelningsklienter med chattfunktioner och multiplayer-spel (särskilt MMORPGs) kallas meddelandeloggar. Dessa loggar sparas vanligtvis i vanliga textfiler, men IM- och VoIP-klienter (t.ex. Skype) kan spara dem i HTML-filer för att underlätta läsningen eller möjliggöra kryptering.
### Serverloggar
Serverlogg är faktiskt en loggfil som innehåller en lista över aktiviteter som utförs och skapas eller underhålls automatiskt av servern själv. Vanligtvis är dessa filer inte tillgängliga för allmänna Internetanvändare, endast för webbansvariga eller annan administrativ person för en Internettjänst.



## Referenser ##

* [Loggfil - Wikipedia](https://en.wikipedia.org/wiki/Log_file)

