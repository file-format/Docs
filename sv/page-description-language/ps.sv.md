{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS-filformat",
  "description":"Läs mer om PS-filformat och API:er som kan skapa och öppna PS-filer.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en .PS-fil? ##

PostScript (PS) är ett allmänt sidbeskrivningsspråk som används i branschen för desktop och elektronisk publicering. Huvudfokus för PostScript (PS) är att underlätta den tvådimensionella grafiska designen. De flesta språk kräver ett distinkt kompileringssteg innan koden körs, medan Post Script (PS)-format stöder en runtime rakt fram tolkning. Dess tidiga version definierar de grafiska formerna, olika textutseende och modellerade bilder på utskrivna sidor eller visade sidor, enligt reglerna för Adobes bildmodell. Ett PS-program kan kommunicera en dokumentbeskrivning mellan en sammansättning och ett utskriftssystem, vilket håller enheten oberoende och på hög nivå. Dessutom kan detta program också styra utseendet på text och grafik på en display.

PostScript-sidbeskrivning är tillgänglig för att renderas, visas på skrivare och annan utdataenhet med hjälp av enhetens PostScript-tolk. Eftersom kommandona för att skriva ut tecken, grafiska former och bilder exekveras av tolk, för den specifika enheten, konverteras PostScript-beskrivningen på hög nivå till rasterdataformatet på låg nivå. I allmänhet är olika applikationer som illustratörer, dokumentkompositionssystem och datorstödd design (CAD) automatiserade för att generera PostScript-sidbeskrivningar. Vanligtvis måste programmerare skriva PostScript-program när nya applikationer skapas. En programmerare kan dock dra fördel av funktionerna i PostScript-språket som inte är tillgängliga i någon applikation genom att skriva ett PS-program för den speciella situationen.

## Kortfattad bakgrund ##

Konceptet med PostScript-språket introducerades först av John Warnock. 1966 arbetade han på ett projekt i New York Harbor. Han försökte utveckla en tolk för en stor tredimensionell grafik för databasen för det projektet. För att bearbeta den här grafiken skapade John Warnock språket Design System. Samtidigt letade Xerox PARC efter ett standardsätt för att definiera sidbilder för sin första laserskrivare. Även om Bob Sproull och William Newman 1975-76 utvecklade pressformatet (dataformat) för att driva laserskrivare, behövdes ändå ett språk för mer flexibilitet. 1978 gick Warnock med Martin Newell i Xerox PARC och skrev om tolkningsspråket JaM som senare växte och utökades till Interpress-språket. Warnock grundade Adobe Systems i december 1982 tillsammans med Chuck Geschke, Doug Brotz, Ed Taft och Bill Paxton. De började arbeta på ett enklare språk kallat PostScript liknande Interpress, som släpptes kommersiellt 1984. Steve Jobs från Apple besökte dem och rådde dem att anpassa PostScript för att driva laserskrivare.

I mars 1985 var den första skrivaren med en inbäddad PostScript-tolk Apples LaserWriter, som revolutionerade desktop publishing (DTP). Den tekniska soliditeten och den utbredda tillgängligheten gjorde PostScript till ett valspråk för stationär och elektronisk publicering. Under 1990 var en tolk för PostScript-språket en väsentlig del av laserskrivarna.

## Huvuddrag ##

PostScript-språkets förmåga att hantera interaktiv grafik och sidbeskrivning har följande funktioner:

**Former:** Godtyckliga till sin natur, kan bestå av raka linjer, kurvor, kvadrater och kubiska kurvor som kan vara både självgenomgående och frånkopplade (i sektioner och hål).

**Målningsoperatorer:** tillåter formkonturerna av valfri tjocklek, färg, fyllning eller låt formen ritas som ett urklipp för att tillåta beskärning av annan grafik.

**Färger:** har mångfald som gråskala, RGB, CMYK och CIE. Speciella typer av färger modelleras som olika egenskaper: dekorfärger, färgkartläggning, jämn skuggning och återkommande mönster.

**Text:** helt integrerad med grafik. Dessutom tillåter Adobes bildbehandlingsmodell att texttecken visas som grafiska former som kan användas av alla vanliga grafikoperatörer.

**Samplade bilder**: extraherade från originalkällor (skannade fotografier) eller kan produceras syntetiskt. PostScript-språket erbjuder olika sätt att återskapa bilder med vilken upplösning som helst och enligt olika färgmodeller på en utenhet.

Ett allmänt programmeringsspråk kan dra fördel av grafiska funktioner PostScript-språk genom att bädda in Ps i dess ramverk. De primitiva datatyperna, såsom siffror, tecken, arrayer och strängar; styrprimitiver, såsom loopar, procedurer och villkor; och vissa okonventionella funktioner, såsom ordböcker, anges i språket. Dessa funktioner underlättar programmerare att skriva kommandon för att anropa operationer på högre nivå. Dessa högnivåoperationer uppfyller behoven för komplexa applikationer. Sådan praxis är mer kompakt och effektiv snarare än att använda en fast uppsättning grundläggande operationer.

Program skrivna i PostScript kan produceras, kommuniceras och tolkas i form av ASCII-källtext. Hela språket kan definieras i form av utskrivbara tecken och blanksteg. Denna representation hjälper programmerare att skapa, manipulera och förstå språket enkelt. Dessutom hölls fillagring och överföring mellan olika datorer och operativsystem bekvämt genom maskinoberoende.

Binärt kodade former av språket är möjliga när programmet garanteras en helt transparent kommunikationsväg till PostScript-tolken. Strikt sammanhållning till ASCII-representationen av PS-program rekommenderas från Adobe för dokumentutbyte eller arkivlagring.

## Versioner ##

PS(.ps) är filtillägget för ett PostScript-dokument. UK National Archives kategoriserar fem kronologiska versioner av PostScript-filen, definierade i DSC-versionen: version 1.0, 2.0, 2.1, 3.0, 3.1. Varje version definierar viktiga strukturerande kommentarer. Encapsulated PostScript File (EPS) är en speciell undertyp av PostScript-fil som använder språket för att specificera en rektangulär grafik. PostScript Language Reference Manual beskriver en EPS som: "En inkapslad PostScript-fil (EPS) är ett PostScript-program som beskriver högst en enskild sida i en form som kan importeras av andra program för att bädda in i ett innehållande dokument." En PostScript-dokumentfil kan kapsla in en EPS-fil i den. En extra användning av PostScript nämns som Display PostScript (DPS). DPS genererar grafik på skärmen genom en grafikmotor som använder PostScript-bildmodell och språk.

## Referenser ##

* [PostScript-formatfamilj](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

