{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru torrent - soubor BitTorrent",
  "description":"Další informace o souborech TORRENT a rozhraních API, která mohou vytvářet a otevírat soubory TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Co je to TORRENT soubor?

Soubor TORRENT je textový soubor, který používá BitTorrent a další P2P (peer-to-peer) programy pro stahování a výměnu obsahu. Obsah ke stažení může zahrnovat dokumenty, videa, hry, filmy a další média dostupná na internetu. Zahrnuje informace o metadatech o obsahu a umístění médií ke stažení. Software jako BitTorrent používá informace z tohoto souboru, jako je název, velikost souboru a struktura složek pro stahování dat. Soubory Torrent lze převést do jiných formátů souborů, jako je [PDF](/cs/pdf/) online.

## Co je Torrenting? Formát souboru TORRENT pro výměnu dat

Torrenting je koncept výměny (stahování a nahrávání) datových souborů pomocí sítě BitTorrent. Na rozdíl od konvenčních serverů, kde se data nahrávají, aby k nim měli přístup a stahovali je ostatní, jsou torrentové soubory získávány a odesílány pomocí torrentové sítě. Když uživatel otevře soubor .torrent v aplikacích, jako je BitTorrent, software začne stahovat obsah souboru po bitech. Pokud má více uživatelů stejný soubor, BitTorrent rozdělí stahování mezi všechny uživatele, aby se proces stahování urychlil. Počítač uživatele, který soubor stahuje, se zároveň stává také zdrojem souboru pro jeho odeslání dalším uživatelům, kteří také stahují stejný soubor.

### Struktura souboru TORRENT

Soubor torrentu je kombinací seznamu souborů a informací o metadatech o všech částech souboru ke stažení. Obsahuje následující informace ve formě klíčů.

- `announce` — URL trackeru, který je oznámen ostatním kolegům, aby informovali o dostupnosti souboru
- `info` — Toto se mapuje na slovník, jehož klíče jsou závislé na tom, zda je sdílen jeden nebo více souborů:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — velikost souboru v bajtech.
- `cesta` — seznam řetězců odpovídajících názvům podadresářů, z nichž poslední je skutečný název souboru
- `length` — velikost souboru v bajtech (pouze když je sdílen jeden soubor)
- `name` — název souboru, kam se má soubor uložit
- `délka kusu` — počet bajtů na kus. To je běžně 28 KiB = 256 KiB = 262 144 B.
- `kusy` — seznam hash, který je zřetězením hash SHA-1 každého kusu.

## Je torrentování bezpečné a legální?

Torrentingový protokol pro výměnu dat mezi uživateli P2P je bezpečný, protože je pouze prostředkem ke sdílení jakéhokoli typu souboru. Proto protokol sám o sobě není nebezpečný nebo nezákonný. Obsah sdílený prostřednictvím sítě však může obsahovat soubory nebo média, která mohou porušovat právní status sdílených dokumentů. V takovém případě může výměna takových údajů způsobit právní kroky proti stranám zapojených do veřejného sdílení takových souborů.

## Reference

* [Soubor TORRENT – wikipedie](https://en.wikipedia.org/wiki/Torrent_file)

