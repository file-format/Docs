{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ a VHDX fájlformátumról és az API-król, amelyek VHDX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"VHDX fájlformátum - Mi az a VHDX fájl?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Mi az a VHDX fájl?

A VHDX fájl egy lemezképfájl a Virtual Hard Disk v2 fájlformátumban. Tartalmaz egy teljes operációs rendszert, amely betölthető és bármely normál gépként használható szoftverek tesztelésére vagy olyan szoftverek futtatására, amelyekhez adott operációs rendszer szükséges. A VHDX annak ellenére, hogy teljes lemezkép, egyetlen fájlban tárolódik. A virtuális gép szoftverei, például a Parallels Desktop, a Windows Virtual Machine és a Virtual Box betölthetik és megnyithatják a lemezképet.

A VHDX fájl konvertálható [VHD](/hu/disk-and-media/vhd/) formátumba a Hyper-V Manager segítségével, vagy [VDI](/hu/disc-and-media/vdi/) formátumba a VirtualBox segítségével.

## VHDX fájlformátum – További információ

A VHDX fájlformátum részletei teljes mértékben dokumentáltak, és online elérhetők [VHDX fájlformátum specifikációi](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) ) a Microsoft dokumentációjában. Ez a VHD formátum kiterjesztése, és továbbfejlesztett képességekkel rendelkezik. A VHDX fájlformátum további szolgáltatásokat biztosít, amelyek a virtuális merevlemezen és a virtuális merevlemezen elérhető fájlrétegekben érhetők el. Jobban optimalizált, és jobb eredményeket ad a tárolóhardver-konfiguráció és -képességek tekintetében. A VHDX fájlok megnyithatók

### Virtuális merevlemezek támogatása VHDX-ben

Háromféle virtuális merevlemezt támogat.

1. **Rögzített virtuális merevlemez** – Virtuális merevlemez rögzített adatmérettel. A virtuális merevlemez mérete nem változik az adatok hozzáadásával vagy eltávolításával.

1. **Dynamic Virtual Hard Disk** - Virtuális merevlemez dinamikus lemezmérettel. A mérete bármikor akkora, mint a ráírt tényleges adatok és a metaadatok. A fájl mérete dinamikusan növekszik az adatok hozzáadásával vagy eltávolításával.

1. **Különböző virtuális merevlemez** – A virtuális merevlemez áramát módosított blokkok halmazaként jeleníti meg, összehasonlítva egy szülő virtuális merevlemez-fájllal.

## Hivatkozások

* [VHDX fájlformátum specifikációi](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD – Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

