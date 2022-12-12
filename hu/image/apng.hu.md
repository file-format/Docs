{
  "date" : "2019-10-11",
  "keywords" :[ "apng fájl", "apng fájlformátum", "mi az apng fájl", "fájl", "apng példa", "apng fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG fájlformátum - animált hordozható hálózati grafikus fájl",
  "description":"További információ az APNG fájlformátumról és az APNG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az APNG fájl?

Az .apng (Animated Portable Network Graphics) kiterjesztésű fájl raszteres grafikai formátum, és a Portable Network Graphic ([PNG](/hu/image/png/)) nem hivatalos kiterjesztése. Több képkockából áll (mindegyik PNG-kép), amelyek egy animációs sorozatot képviselnek. Ez hasonló megjelenítést biztosít, mint egy [GIF](/hu/image/gif/) fájl. Az APNG fájlok támogatják a 24 bites képeket és a 8 bites átlátszóságot. Az APNG visszafelé kompatibilis a nem animált GIF fájlokkal. Az APNG-fájlok ugyanazt a .png kiterjesztést használják, és olyan alkalmazásokkal nyithatók meg, mint a Mozilla Firefox, az APNG-támogatással rendelkező Chrome, az iOS 10 rendszerhez készült iMessage alkalmazások.

## Rövid története

* Az APNG specifikációkat 2004-ben hozták létre az animált PNG képek támogatására
* Az APNG dekódereket sokkal kisebb méretben fejlesztették ki, a PNG dekóder hátuljának felhasználásával
* Folyamatos mérlegelés után egy új MIME típusú kép/apng került megfogalmazásra, miközben a kiterjesztést nem .apng, hanem a .png kiterjesztéssel változtattuk meg.
* Az APNG-t a PNG csoport 2007. április 20-án hivatalosan elutasította, mivel egységes a PNG-képekkel, ugyanakkor eltérő specifikációi vannak.

## APNG fájlformátum

Az APNG fájlok bináris fájlokként vannak tárolva a lemezen, és az animált képekhez a PNG kiterjesztett specifikációit használják. Az APNG-fájl első kerete egy normál PNG-adatfolyam, amelyet a PNG-dekóderek képesek megjeleníteni. Az APNG-fájlformátum követi a PNG-specifikációkat, és az adatok szelvényekben, úgynevezett darabokban tárolódnak. Az APNG azonban a következő új darabokat vezette be:

"Animation Control Cunk (acTL)" – Azt jelzi, hogy ez a fájl egy animált PNG-fájl, nem pedig egy normál PNG-fájl. Jelölőként működik, és az IDAT csonk elé kerül. Tartalmazza a képkockák számát és az animációk ismétlésének idejére vonatkozó információkat is

"Frame Control Cunk" - Minden egyes metaadat-információ, például méretek, pozíció, átlátszósági alkalmazás, valamint az előző vagy a következő képkockával való helyettesítési információ az elején fordul elő.

"Frame Data Cunk" - A keret tartalmát tárolja, és egy sorszámmal kezdődik. Ennek a sorszámnak a szerkezete megegyezik az alapértelmezett kép IDAT-darabjával.

{{< figure src="../APNG.png" alt="Animált PNG – APNG fájlformátum" >}}

Az APNG visszafelé kompatibilis a PNG-vel, mivel az oldalsó specifikációit úgy tervezték meg, hogy a PNG-fájlt olvasó alkalmazásnak egyszerűen figyelmen kívül kell hagynia azokat a darabokat, amelyeket nem ért. A bitmélységre, színtípusra, tömörítésre, szűrőkre, sorváltási módszerekre és palettainformációkra vonatkozó specifikációk ugyanazok, mint az alapértelmezett PNG formátum.

## APNG vs GIF

Mivel a GIF már a helyén van, és hosszú ideig használatban van, felmerülhet a kérdés, miben különbözik az APNG a GIF-től. Az alábbiakban bemutatjuk az APNG és a GIF összehasonlítását, amely rövid képet ad mindkét fájlformátumról.

||APNG|GIF|
---|---|---|
|Megjelent|2004|1987|
|Színmélység|24 bit|8 bit|
|Frame Rate|Korlátlan|10 képkocka másodpercenként|
|Átláthatóság|Teljes és részleges|Teljes|
|Tömörítés|Nagyon jó|Jó|

## Hivatkozások

* [APNG fájlformátum](https://en.wikipedia.org/wiki/APNG)
* [A PNG formátum hivatalos specifikációi](https://www.w3.org/TR/PNG/)

