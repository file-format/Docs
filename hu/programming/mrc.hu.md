{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "file", "extension", "file format", "mrc implementáció", "Programozási útmutató", "mrc példa", "mIRC", "mIRC scripting language", "Files of INI", " mSL szkriptnyelv", "mIRC nyelv", "mIRC szkriptek", "szkriptnyelv" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC Script Language File",
  "description":"További információ az MRC fájlformátumról és az API-król, amelyek MRC fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Mi az MRC fájl?

Az mIRC egy szkriptnyelv, amely IRC-kliensként (Internet Relay Chat) van beágyazva a Windows operációs rendszerbe. Védelmet nyújt a kéretlen levelekkel szemben személyes és csatornás használatra. A felhasználói kompatibilitás jobb élményének biztosítása érdekében ez a mIRC szkriptnyelv lehetővé teszi párbeszédablak létrehozását. A szkripteket tartalmazó, többnyire egyszerű szöveges fájlok MRC kiterjesztéssel vagy [INI](/hu/system/ini/) fájlként kerülnek tárolásra. Ennek a nyelvnek a funkcióit parancsoknak és azonosítóknak nevezzük (amikor értéket adnak vissza).

Az mIRC nyelv több szkriptfájl egyidejű betöltését teszi lehetővé. Másrészt az egyik fájl miatt előfordulhat, hogy a másik nem használható, ha egyidejűleg betöltődik. A parancsok mentésre kerülnek, és automatikusan létezhetnek az IRC-ben. Az ezen a nyelven használt parancsok és álnevek nem élvezik a karakterek elsőbbségét.

Az mIRC-t széles körben használják arra, hogy a botok automatikusan kezeljenek egy csatornát, de az mSL szkriptnyelvvel is módosítható. Számos új funkciót vezethet be, például makrókat, zenelejátszási képességet, kis makrókat és funkciókat, alapjátékokat vagy kis alkalmazások működtetését.


## Rövid története ##

Ezt a szkriptnyelvet először 1995-ben fejlesztette ki Khaled Adam Bey. A szkriptnyelv kialakítását is Khalid készítette. Ennek a nyelvnek a célja az eseményvezérelt programozás volt. Kezdetben ennek a programozási nyelvnek a fájlkiterjesztése .mrc és .ini volt. Sőt, saját szoftver licence alapján fejlesztették ki.

## Műszaki specifikáció ##

Egyes funkciókat ezen a mIRC nyelven keresztül egyedi szkriptek írják le, és álnevekként ismertek. Amikor ezek az álnevek értékeket adnak vissza, egyéni azonosítóknak nevezzük őket. Az ebben a mIRC nyelvben található összes változó dinamikusan van beírva. A jeleket az mIRC szkriptek használják. Ennek a szkriptnyelvnek egy másik jellemzője a felugró ablakok. A felhasználók egyszerűen kiválaszthatják a felugró ablakokat. A távirányítók bizonyos eseményekhez vannak megadva. A távirányítók a relatív esemény bekövetkezésekor hívódnak meg.

A szóközzel elválasztott tokenek a nyelv minden kódsorának törésére szolgálnak. Vannak más népszerű kiterjesztések is, amelyeket az mIRC fájlokhoz használnak, például az MDX (mIRC Dialog Extension) és a DCX (Dialog Control Extension). Mindkettő párbeszéd-kiterjesztés, és viszonylag népszerűbb. A nyelvi konstrukciókra ennek a szkriptnyelvnek a nómenklatúrája hivatkozik. A mIRC nyelv a szkriptnyelv különböző aspektusait tartalmazza, például helyi és globális változókat, bináris változókat, hash táblákat és fájlkezelést.


## MRC fájlformátum példa ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/hu/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Hivatkozási szám

* [MIRC – a Wikipedia által](https://en.wikipedia.org/wiki/MIRC_scripting_language)



