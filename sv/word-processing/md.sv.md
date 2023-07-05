{
  "date" : "2019-10-11",
  "keywords" :[ "md-fil", "md-filformat", "vad är en md-fil", "fil", "md-exempel", "md-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown Language File",
  "description":"Läs mer om MD-filformat och API:er som kan skapa och öppna MD-filer.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en MD fil?

Textfiler skapade med Markdown-språkdialekter sparas med filtillägget **.md** eller **.MARKDOWN**. MD-filer sparas i vanligt textformat som använder Markdown-språket som även inkluderar inline textsymboler, som definierar hur en text kan formateras såsom indrag, tabellformatering, typsnitt och rubriker. MD-filer kan konverteras till HTML med ett program som heter Markdown. Markdown-språket släpps av John Gruber.

MD-filer kan också kategoriseras som utvecklarfiler som oftast används av Markdown, för att konvertera textfiler till HTML-versioner så att användare kan skapa filer som är lätta att läsa och skriva. Följande är de program som kan öppna en .md-fil:

* Microsoft Notepad
* Anteckningsblock2
* Apple TextEdit
* Microsoft WordPad

Ett varningens ord är att inte byta namn på filtillägget för .md-filer. Om så är fallet kommer detta inte att ändra filtypen eftersom det finns speciella konverteringsprogram tillgängliga för att ändra en fil från en filtyp till en annan. Som diskuterats ovan är .MD-filer tilläggen av filer som skapats i Markdown-språkprogramvaran. **Markdown** är ett [lätt märkningsspråk](https://en.wikipedia.org/wiki/Lightweight_markup_language) avsett för ett syfte, för att användas för att formatera text på webben med syntax för vanlig textformatering. Låt det vara tydligt att Markdown inte är en ersättning för HTML eftersom dess syntax är mycket liten och innehåller en mycket liten delmängd av HTML-taggar. Anledningen bakom Markdown är att göra det enkelt att läsa, skriva och redigera prosa. Med andra ord kan vi säga att HTML är ett publiceringsformat medan Markdown är ett skrivformat.

Markdown är nu ett av världens mest populära märkningsspråk. När du använder Microsoft Word, formateras ord och fraser genom att klicka på knappar och ändringar är omedelbart synliga. Men Markdown är inte så. När Markdown-formaterad fil skapas läggs Markdown-syntax till i texten för att indikera vilka ord och fraser som kan se annorlunda ut. Till exempel, för att visa en rubrik, läggs ett nummertecken till före den (t.ex. # Rubrik ett). För att göra en fet mening läggs två asterisker till före och efter den (t.ex. **den här texten är fetstilt**). Markdown-syntax kan ses efter ett tag i texten.

## Kortfattad bakgrund

John Gruber och Aaron Swartz 2004 skapade Markdown-språket med idén att göra det möjligt för människor att "skriva med lättläst och lättläst textformat och med möjligheten att konvertera det till XHTML eller HTML. Målet bakom dess design är läsbarhet – språket är läsbart som det är, utan att se ut som om det har taggats eller lagts till med formateringsinstruktioner som görs i märkningsspråk som RTF eller HTML där taggar och formateringsinstruktioner är uppenbara. Den grundläggande inspirationen är att använda befintliga konventioner för att markera vanlig text i e-post.

Sedan dess har Markdown återimplementerats av andra, liksom i en Perl [modul](https://en.wikipedia.org/wiki/Modular_programming) tillgänglig på [CPAN](https://en.wikipedia.org/ wiki/CPAN) och på olika andra programmeringsspråk. Den distribueras under en [BSD-liknande licens](https://en.wikipedia.org/wiki/BSD_license) och ingår i, eller tillgänglig som en plugin för, flera [innehållshanteringssystem](https:// en.wikipedia.org/wiki/Content_management_system).

## Tekniska specifikationer

När något skrivs i Markdown lagras texten först i en vanlig textfil med filändelsen .md eller .markdown, sedan används markdown-applikation som Dillinger för bearbetning av Markdown-fil för att konvertera Markdown-formaterad text till HTML för att visa den på webben webbläsare. Markdown-applikationer använder en //Markdown-processor// (kallas även ofta för en "parser" eller en "implementation") för att ta den Markdown-formaterade texten och mata ut den till HTML-format. Flödesdiagrammet för processen är som nedan:

Kort sagt är det en process i fyra steg som följer:

1. Skapa först Markdown-filer med en textredigerare eller Markdown-applikation med tillägget .md eller .markdown.
1. Markdown-filen öppnas sedan i en Markdown-applikation.
1. Markdown-applikationen används för att konvertera Markdown-filen till ett HTML-dokument.
1. HTML-filen visas sedan i en webbläsare eller så används Markdown-applikationen för att konvertera den till ett annat filformat, som PDF.

Markdown är snabbt och enkelt att ta anteckningar, skriva innehåll för webbplats, producera tryckfärdiga dokument, för att publicera böcker, generera presentationer och göra dokument.

Vissa av versionerna i markdown hade en betydande inverkan på andra versioner så mycket att man ofta kommer att se dem citerade som en del av andra versioner. Till exempel nämner biblioteken stöd för CommonMark (GFM). Låt oss ta en kort titt på dem.

### GFM
Markdown är så populärt bland utvecklare eftersom den öppna källkodsdelningsplattformen Github accepterade och utökade språket med en version som heter Github Flavored Markup (GFM) som inkluderar inhägnade kodblock, URL-aultolinking, genomstrykning, tabeller och skapa uppgifter.

### CommonMark
Markdown-utvecklare försökte nyligen standardisera markdown, de gick samman för att skapa en version, tester och dokumentation för språket som är mer robust och kallas CommonMark. Det här formatet är lite nytt och stöder inte många funktioner, men snart kommer många MultiMarkdown-funktioner att läggas till.

### Multi-Markdown
Multi-Markdown lade till olika funktioner till språket som stöds av andra versioner. Ursprungligen skrevs den i Perl, men flyttades senare till C. Den stöder inhägnade kodblock, syntaxmarkering, tabeller, metadata, fragment/korsreferenslänkar, fotnoter, genomstrykning, definitionslistor, matematik.

## Referenser

* [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

