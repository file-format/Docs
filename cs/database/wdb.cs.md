{
  "date" : "2021-08-24",
  "keywords" :[ "soubor wdb", "formát souboru wdb", "co je soubor wdb", "soubor", "příklad wdb", "přípona souboru wdb", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů WDB a rozhraních API, která mohou vytvářet a otevírat soubory WDB.",
  "title" :"WDB - SQL Server Trace File",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Co je soubor WDB?
Soubor s příponou .wdb je ve skutečnosti databázový soubor vytvořený společností Microsoft Works, který se používal k provádění funkcí, jako je systém správy databáze. Soubor WDB je podobný souboru databáze Access ([MDB](/cs/database/mdb/)), ale je méně účinný a má větší omezení. Soubory WDB nelze otevřít pomocí aplikace Microsoft Access. Můžete však otevřít soubor WDB v Microsoft Works a poté jej exportovat do souboru MDB, aby bylo možné otevřít soubor WDB v MS Access.

## formát souboru WDB
Microsoft Works Database je nativní databázový formát kancelářského balíku Microsoft Works. Kvůli proprietární povaze formátu a některým omezením. Soubory WDB nelze otevřít v žádném jiném softwaru než Microsoft Works. Ve formátu souboru lze před každým textovým řetězcem ASCII, který představuje hodnoty polí, které byly ukončeny hodnotou NULL, nalézt opakující se 10bajtové záhlaví. Záhlaví obvykle začíná **\x0f** bajtem a NULL, po kterém následují 4 datové bajty střídané hodnotami NULL.

### Struktura souboru

Struktura souboru WDB je uvedena níže:
- **1. hlavička**: od začátku souboru, končící \x25\x00\xf2 a 244 NULL bajty
- **2. záhlaví**: začíná \xffT - tj. \xff\x54 a rozšiřuje se na 4096 bajtů, které obsahuje názvy sloupců/polí a další věci a zdá se, že začíná na pozici 6144 bajtů.
- **Pole**: hodnota má 10bajtové záhlaví s následujícím formátem: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , část 2} {db 4} \x00. datový bajt 2 je číslo pole, datový bajt 3 je číslo záznamu (přidání datového bajtu 3, část 2, když překročí 256 záznamů).


## Reference ##

* [Formát User:JesseW/wdb](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

