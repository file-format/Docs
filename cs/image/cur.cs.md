{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "přípona", "soubor", "formát", "obrázek", "Bitmapa nezávislá na zařízení", "Formát souboru kurzoru", "Kurzor", "Windows", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Formát souboru kurzoru",
  "description":"Další informace o formátu souboru CUR a rozhraních API, která mohou vytvářet a otevírat soubory CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor CUR? ##

Soubor CUR je statický formát souboru kurzoru Microsoft Windows. V podstatě jsou to stacionární obrázky identické se soubory ICO (ikony) ve všech směrech kromě přípony. CUR i [ICO](/cs/image/ico/) jsou stanoveny na základě specifikace bitmap nezávislé na zařízení [DIB](/cs/image/dib/) (bitmap nezávislá na zařízení). Výchozí, stejně jako vlastní kurzor, jako je ukazatel myši Windows pro operační systém Windows, jsou uloženy v souborech CUR. Může to být šipka pro běžné použití, rotující přesýpací hodiny pro demonstraci čekacích lhůt nebo I-bar pro úpravu textu. Soubory CUR se dodávají spolu s instalačním balíčkem vlastních motivů plochy, aby se zajistilo, že kurzor Windows odpovídá vlastnímu motivu plochy.

## Technické specifikace ##

Soubory CUR jsou binární systémové soubory, které lze nalézt na zařízeních fungujících v operačním systému Microsoft Windows. Obrázky ukazatele CUR přicházejí v různých standardních velikostech, jako je 16×16, 32×32 atd. Soubory CUR jsou velmi podobné souborům ICO; oba se skládají z malých stacionárních obrázků. Liší se pouze přípona souborů CUR a ICO. Kromě toho se vysvětlení aktivního bodu v záhlaví souboru CUR liší od souboru ICO. Aktivní bod interpretuje posun pixelů od levého horního rohu k místu, kam ukazujete myší. Systémy Windows stále používají soubory CUR, ale nyní mají animované kurzory obvykle příponu souboru ANI namísto CUR.

## Stručná historie ##

Soubor CUR je vytvořen ze souboru ICO. První formát souboru CUR byl začleněn do operačního systému Microsoft Windows 1.0 v roce 1981, aby usnadnil komerční využití. Brzy byly představeny další interaktivní kurzory, které uživatelům umožnily upravit předvolby kurzoru z dostupných předinstalovaných možností. Je však snadné upravit soubor CUR sami, i když nemáte dostatečné technické znalosti.


## Příklad CUR ##

Soubory CUR lze nalézt na *C:\Windows\Cursors*:

{{< figure src="../cur.png" alt="Formát souboru CUR" >}}

