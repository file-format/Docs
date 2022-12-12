{
  "date" : "2021-10-20",
  "keywords" :[ "soubor sfar", "formát souboru sfar", "co je soubor sfar", "soubor", "příklad sfar", "přípona souboru Mass Effect 3 DLC", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru SFAR Mass Effect 3 a rozhraních API, která mohou vytvářet a otevírat soubory SFAR.",
  "title" :"SFAR - Mass Effect 3 DLC soubor",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Co je soubor SFAR?

Soubor s příponou .sfar je herní datový soubor používaný Mass Effect 3 k uložení DLC (obsahu ke stažení) v komprimovaném, proprietárním archivu. Mass Effect 3 je hra vytvořená společností Electronic Arts, přední společností zabývající se vývojem her. Obsah DLC uložený v souboru SFAR se používá k rozšíření hry o další obsah a funkce.

## Formát souboru SFAR – Další informace

Soubory SFAR se ukládají/ukládají jako komprimované archivní soubory v binárním formátu souboru. Ty používají pro kompresi obsahu jak LZX, tak LZMA kompresní algoritmy. Soubory SFAR lze otevřít pomocí editoru DLC, který je součástí balení ME3 Explorer. Kromě SFAR může DLC Editor extrahovat další herní soubory, jako je [PCC](/cs/game/pcc/).

## Specifikace formátu souboru SFAR

Soubor SFAR je rozdělen do následujících čtyř hlavních částí.

### Záhlaví SFAR

Záhlaví SFF obsahuje informace o různých částech, které tvoří soubor.

### Tabulka souborů SFAR

Tabulka souborů SFAR obsahuje seznam položek souborů, kde každá položka je dlouhá 30 bajtů.

### Tabulka velikosti bloku

Block-Size obsahuje více položek, přičemž každá položka je dlouhá 2 bajty. Tato hodnota určuje velikost bloku odpovídající položce v tabulce souborů.

### Bloky

Blokové bloky v souboru SFAR obsahují data uvnitř souboru SFAR.

## Reference

* [Formát souboru DLC SFAR – výzkum](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

