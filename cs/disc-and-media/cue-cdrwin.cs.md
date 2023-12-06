{
"date":"2023-10-18",
   "keywords":[
"tágo",
"soubor cue",
"soubor cue cdrwin cue sheet",
"jak otevřít soubor cue",
"soubor",
"přípona souboru cue",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CUE - CDRWIN Cue Sheet",
   "description":"Další informace o formátu souboru CUE CDRWIN Cue Sheet a rozhraních API, která mohou vytvářet a otevírat soubory CUE.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## Co je soubor CUE?

Soubor **.CUE**, také známý jako **CDRWIN Cue Sheet**, je prostý textový soubor, který obsahuje informace o stopách a rozložení obrazu zvukového CD nebo disku, obvykle ve formátu BIN nebo ISO. Tyto soubory se často používají k popisu struktury a obsahu disku, což umožňuje softwaru pro vypalování CD nebo softwaru virtuální jednotky přesně reprodukovat původní disk.

## Příklad souboru CUE

Zde je příklad toho, jak může soubor „.cue“ vypadat:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Sheet

CDRWIN Cue Sheet je specifická variace formátu souboru ".cue" používaného softwarem CDRWIN. CDRWIN je software pro vypalování a vytváření CD/DVD a jeho „.cue“ listy jsou navrženy pro použití s tímto softwarem. Tyto ".cue" listy obsahují informace nezbytné pro CDRWIN k přesnému vytvoření nebo vypálení CD nebo DVD.

Zde jsou některé klíčové detaily specifické pro CDRWIN Cue Sheets:

1. **Unikátní pro CDRWIN**: Listy ".cue" CDRWIN jsou proprietární formát specifický pro software CDRWIN. I když sdílejí podobnosti se standardními soubory ".cue", jsou přizpůsobeny pro práci s funkcemi a nastaveními CDRWIN.
    






2. **Uživatelsky přívětivé rozhraní**: CDRWIN poskytuje snadno použitelné rozhraní pro vytváření a úpravu svých „.cue“ listů. Uživatelé mohou přidávat nebo upravovat informace o stopách, indexech, mezerách a dalších parametrech uživatelsky příjemným způsobem.
    






3. **Kompatibilní typy disků**: Cue Sheets CDRWIN se používají především k vytváření různých typů disků CD a DVD, včetně datových disků, zvukových disků CD, disků se smíšeným režimem a dalších. Formát umožňuje uživatelům specifikovat typ a obsah disku, který chtějí vytvořit.
    






4. **Ovládání rozložení disku**: Cue Sheets CDRWIN poskytují podrobnou kontrolu nad rozložením a strukturou disku, včetně pořadí skladeb, nastavení pauzy/mezery a jakýchkoli dalších specifických preferencí uživatele.
    






5. **Podpora ISO a BIN**: CDRWIN může pracovat s obrazovými formáty disků ISO i BIN. List ".cue" specifikuje, který obrazový soubor je použit pro disk, což zajišťuje správnou synchronizaci mezi cue a obrazem.
    






6. **Burning and Ripping**: Tyto „.cue“ listy jsou klíčové při vypalování disků nebo ripování stop z disků pomocí CDRWIN. Pomáhají zajistit, aby konečný produkt odpovídal zamýšlenému rozvržení a obsahu.
    






7. **Backup and Restoration**: Uživatelé CDRWIN často vytvářejí „.cue“ listy při zálohování svých CD nebo DVD. Tyto listy lze později použít k obnovení obsahu disku, včetně rozložení stopy a načasování.

## Jak otevřít soubor CUE?

Cue Sheets CDRWIN jsou speciálně navrženy pro software CDRWIN, takže jsou obvykle určeny k otevření a použití v rámci CDRWIN.

Programy, které otevírají nebo odkazují na soubory CUE

- CDRWIN
- Inteligentní projekty IsoBuster
- EZB Systems UltraISO

## Další soubory CUE

Zde jsou další typy souborů, které používají příponu souboru **.cue**.

**Disk a média**
- [CUE - Cue Sheet File](/cs/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/cs/disc-and-media/cue-cdrwin/)

## Reference
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

