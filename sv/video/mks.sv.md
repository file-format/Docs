{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS filformat",
  "keywords" :[ "mks", "matroska video", "mkv-format", "fil", "format", "video"],
  "description":"Läs mer om MKS-filformat för undertexter endast skapade av Matroska och API:er som kan skapa och öppna MKS-filer.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Vad är en MKS fil?

MKS-filerna är allmänt kända som Matroska-filer som endast innehåller undertexter. Även om Matroska är en allmän filbehållare, undviker den att behålla informationen i specifika format. Eftersom undertexter används i vissa av ljud- eller videobehållarna, lägger Matroska uppmärksamhet på att lagra några vanliga undertextformat. Det hjälper Matroska att vara konsekvent med tillväxttakten. Du måste följa punkterna nedan för att lagra undertexterna i Matroska:

- ".mks". tillägget kommer att användas av Matroska-filen (som endast innehåller undertexter).
- **CodecPrivate** används för att lagra all codec-relaterad information som är global för en hel ström.
- Ta bort start- och stopptidsstämplarna som används i ett inbyggt tidsstämpellagringsformat. Använd istället Blocks tidsstämpel och Duration.
- Du kan använda vad som helst med ett transparent lager, inklusive en video.

## Vanliga undertextformat

Här är några korta anteckningar om vanligare undertextformat som lagras i Matroska:

### Bilder Undertexter
VobSub undertextformatet är det första bildtextformatet som importeras till Matroska. Detta format genereras genom att exportera undertexterna från en DVD. Spåren bör separeras under lagring i Matroska om VobSub består av en uppsättning av flera strömmar.

### SRT-undertexter
SRT är det enklaste och mest grundläggande av alla undertextformat. Den består av fyra delar enligt nedan:
 



1. En siffra som anger sekvensen för undertexten.
2. Undertextens uppträdande och försvinnande tid på skärmen.
3. Själva undertexten.
4. En tom rad för att indikera början på nästa undertext.
 



### SSA/ASS-undertexter
Sub Station Alpha (SSA) är ett filformat som används av den populära undertextredigeraren SubStation Alpha. SSA-undertexterna används ofta av fans. Den har möjlighet att visa moderna funktioner, t.ex. karaoke, positionering, styling, etc.
 



### WebVTT-undertexter
World Wide Web Consortium (W3C) utvecklade WebVTT som förkortas som "Web Video Text Tracks Format". Detta format används för att markera externa textspårresurser i samband med HTML-elementet.

### HDMV presentation grafik undertexter
HDMV presentation graphics subtitle format (HDMV PGS) är en serie av bitmappar och vi kan inte säga det text alls. Med andra ord kan man säga att det bara är en tidsinställd sekvens av grafiska bilder. För att extrahera informationen är konvertering av PGS till SRT en nödvändig process.

### HDMV text undertexter
HDMV-texten är känd som textformatet som används på Blu-rays. Matroska tillåter endast UTF-8 teckenuppsättning When lagrar TextST-undertexterna.

### Digital Video Broadcasting (DVB) undertexter
DVB-undertextformatet introducerades för att reglera sändningen och visningen av flera språk undertextning på TV-signaler. Ett typiskt undertextningsformat skulle också tillåta alla tittare att titta på DVB-textade sändningar, oavsett vilken tillverkare av överföringssystemen är.


## Referenser ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

