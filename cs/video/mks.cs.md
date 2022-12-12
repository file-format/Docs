{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MKS",
  "keywords" :[ "mks", "matroska video", "formát mkv", "soubor", "formát", "video"],
  "description":"Další informace o formátu souboru MKS pro titulky vytvořené pouze Matroskou a rozhraními API, která mohou vytvářet a otevírat soubory MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Co je soubor MKS?

Soubory MKS jsou obecně známé jako soubory Matroska obsahující pouze titulky. Přestože je Matroska obecný kontejner souborů, vyhýbá se uchovávání informací o konkrétních formátech. Vzhledem k tomu, že se v některých audio nebo video kontejnerech používají titulky, Matroska věnuje pozornost ukládání některých běžných formátů titulků. Pomáhá Matrosce být v souladu s tempem růstu. Chcete-li uložit titulky v Matrosce, musíte postupovat podle níže uvedených bodů:

- „.mks“. příponu bude používat soubor Matroska (obsahující pouze titulky).
- **CodecPrivate** se používá k ukládání všech informací souvisejících s kodeky, které jsou globální pro celý stream.
- Odstraňte počáteční a koncová časová razítka, která se používají v nativním formátu úložiště časových razítek. Místo toho použijte časové razítko Bloky a Trvání.
- Můžete použít cokoli s průhlednou vrstvou, včetně videa.

## Běžné formáty titulků

Zde je několik krátkých poznámek o běžnějších formátech titulků uložených v Matrosce:

### Titulky obrázků
Formát titulků VobSub je prvním formátem obrazových titulků, který lze importovat do Matrosky. Tento formát je generován exportem titulků z DVD. Pokud se VobSub skládá ze sady více streamů, měly by být stopy při ukládání v Matrosce odděleny.

### Titulky SRT
SRT je nejjednodušší a nejzákladnější ze všech formátů titulků. Skládá se ze čtyř částí, jak je uvedeno níže:
 



1. Číslo, které označuje pořadí titulků.
2. Čas zobrazování a mizení titulků na obrazovce.
3. Samotný podtitul.
4. Prázdný řádek označující začátek dalšího titulku.
 



### Titulky SSA/ASS
Sub Station Alpha (SSA) je formát souboru používaný populárním editorem titulků SubStation Alpha. SSA titulky jsou široce používány fanoušky. Má schopnost zobrazovat moderní funkce, např. karaoke, polohování, styling atd.
 



### Titulky WebVTT
World Wide Web Consortium (W3C) vyvinulo WebVTT, který je zkrácen jako „Web Video Text Tracks Format“. Tento formát se používá k označení externích zdrojů textové stopy ve spojení s prvkem HTML.

### HDMV prezentační grafické titulky
Formát HDMV prezentačních grafických titulků (HDMV PGS) je řada bitmap a nemůžeme to vůbec říct text. Jinými slovy, můžete říci, že je to jen časovaná sekvence grafických obrázků. Chcete-li získat informace, převod PGS na SRT je nezbytným procesem.

### HDMV textové titulky
Text HDMV je známý jako formát textových titulků používaný na discích Blu-ray. Matroska umožňuje pouze znakovou sadu UTF-8, když ukládá titulky TextST.

### Digital Video Broadcasting (DVB) titulky
Formát DVB titulků byl zaveden pro regulaci přenosu a zobrazení titulků v několika jazycích na televizních signálech. Typický formát titulků by také umožnil každému divákovi sledovat DVB titulkované přenosy, bez ohledu na to, jaký je výrobce přenosových systémů.


## Reference ##

- [Titulky Matrosky](https://www.matroska.org/technical/subtitles.html)

