{
"datum": "2023-05-16",
  "keywords": [
"sami soubor",
"co je soubor sami",
"příklad souboru sami",
"soubor",
"přípona souboru sami",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru SAMI – soubor pro výměnu titulků a metadat",
  "description":"Další informace o formátu SAMI a rozhraních API, která mohou vytvářet a otevírat soubory SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Co je soubor SAMI?

Soubor s příponou „.sami“ obvykle odkazuje na soubor SAMI (Subtitles And Metadata Interchange). SAMI je formát titulků používaný pro zobrazování titulků nebo skrytých titulků ve videích. Původně byl vyvinut společností Microsoft pro jejich Windows Media Player.

Soubory SAMI obsahují informace o časování a textový obsah pro titulky nebo skryté titulky, což umožňuje jejich synchronizaci s přehráváním videa. Formát podporuje základní možnosti formátování, jako je styl písma, barva a umístění titulků na obrazovce.

Soubory SAMI jsou obvykle soubory ve formátu prostého textu a lze je otevřít a upravit pomocí textového editoru. Obsah souboru SAMI obvykle zahrnuje sekci záhlaví, která poskytuje informace o souboru, za níž následují jednotlivé položky titulků s jejich příslušným časováním a textem.

Zde je příklad toho, jak může soubor SAMI vypadat:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Soubory SAMI se běžně používají ve spojení s přehrávači videa nebo přehrávači médií, které podporují zobrazení titulků, jako je Windows Media Player nebo VLC Media Player. Přehrávač čte soubor SAMI a synchronizuje titulky s obsahem videa, což umožňuje divákům číst titulky při sledování videa.

## Podporované HTML tagy

Soubory SAMI (Subtitles And Metadata Interchange) podporují omezenou sadu tagů podobných HTML pro formátování a styling titulků. Zde jsou některé z běžně používaných značek podporovaných SAMI:

- "."<SAMI> :`` Kořenový prvek, který zapouzdřuje celý soubor SAMI.
- "."<HEAD> :`` Obsahuje informace záhlaví pro soubor SAMI.
<html>- "."<TITLE> :`` Určuje název souboru SAMI. </html>
- "."<BODY> :`` Uzavře položky titulků a jejich informace o časování.
- "."<SYNC> :`` Představuje synchronizační bod pro položku titulků. Určuje čas, kdy se mají titulky zobrazit.
- "."<P> :`` Uzavře skutečný textový obsah titulků. Obvykle se používá v rámci a<SYNC> blok.
<html>- `` <FONT>:`` Definuje vlastnosti písma pro uzavřený text. Atributy jako Barva, Obličej, Velikost a Styl lze použít k úpravě vzhledu písma.</font>
- "."<BR> :`` Vloží zalomení řádku do titulku.
<html>- `` <B>:`` Vykreslí přiložený text tučně.</b>
<html>- `` <I>:`` Vykreslí uzavřený text kurzívou.</i>
<html>- `` <U>:`` Vykreslí přiložený text podtržený.</u>
- "."<C> :`` Určuje polohu nebo zarovnání textu titulků na obrazovce. Podporuje atributy jako Center, Middle, Left, Right, Top, Bottom a jejich kombinace.
- "."<LANG> :`` Určuje kód jazyka pro text titulků. Pomáhá při identifikaci jazyka titulků.

Toto jsou některé ze základních značek podporovaných soubory SAMI. Je důležité si uvědomit, že SAMI nepodporuje celý rozsah HTML tagů a atributů. Podporované značky se primárně zaměřují na stylování a umístění titulků spíše než na poskytování rozsáhlého strukturování dokumentu nebo interaktivity.

## Reference
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

