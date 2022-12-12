---
date: 2019-10-11
keywords: toml, .toml, toml fájlformátum, toml fájlok megnyitása, .toml kiterjesztése, toml kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML fájlformátum
linktitle: TOML
description: "Ismerje meg a TOML fájlformátumot és az API-kat, amelyek TOML fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Mi az a TOML fájl? ##

A TOML (Tom's Obvious Minimal Language) egy minimális konfigurációs fájlformátum, amely .toml kiterjesztést használ. A TOML célja, hogy könnyen olvasható legyen, egyértelműen leképezhető legyen a szótárakba, és hogy könnyen értelmezhető legyen a különböző adatstruktúrákra. A TOML nyílt forráskódú specifikációval rendelkezik, amely közösségi hozzájárulásokat kapott. A TOML-t számos programozási nyelv támogatja, mint például a C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift stb. A TOML fájlok MIME típusa *application/toml*.


## TOML fájlformátum ##

A TOML-fájlok főként kulcs/érték párokból, szakaszokból/táblázatokból, megjegyzésekből állnak, és érvényes UTF-8 kódolású Unicode-dokumentumnak kell lenniük. A TOML támogatja a String, Integer, Float, Boolean, Datetime, Array és Table (hash tábla/szótár) adattípusokat. A TOML nyelv megkülönbözteti a kis- és nagybetűket.

### Szintaxis ###

- **Kulcs-érték párok**: A kulcs-érték párokat egyenlőségjel (=) választja el. Minden párnak új sorban kell lennie.

``` toml
first = "Tom"
utolsó = "Preston-Werner"
```

- **Megjegyzések**: A megjegyzések a hash (#) szimbólummal kezdődnek.

``` toml
# Ez egy TOML dokumentum.
```

- **Strings**: A karakterláncokat idézőjelek (") veszik körül.

``` toml
string = "Példakarakterlánc"
```

- **Többsoros karakterláncok**: A többsoros karakterláncokat három idézőjel („"") veszi körül.

``` toml
[lakcím]
utca = """123 Tornado Alley
Lakosztály 16"""
város = "East Centerville"
állapot = "KS"
```

- **Egész számok/úszók**

``` toml
egész = 20
úszó = 20,5
```

- ** Booleans**: A logikai értékek mindig kisbetűk.

``` toml
bool1 = igaz
bool2 = hamis
```

- **Dátum-Idő**: A DateTime beállításhoz használhat RFC 3339 formátumú dátum-időt az alábbi példában látható módon.

``` toml
eltolási_dátum_idő = 1979-05-27 07:32:00Z
helyi_dátum_idő = 1979-05-27T07:32:00
helyi_dátum = 1979.05.27
helyi_idő = 07:32:00
```

- **Tömbök**: A tömböket szögletes zárójelek veszik körül, az elemeket vesszővel (,) elválasztva.

``` toml
színek = [ "piros", "sárga", "zöld"]
```

- **Táblázatok**: A táblák kulcs/érték párok gyűjteményei, amelyeket fejlécek határoznak meg egy új sorban, szögletes zárójelekkel ([]). A táblázat akkor ér véget, amikor új fejléc kerül megadásra, vagy amikor a fájl véget ér.

``` toml
[lakcím]
utca = """123 Tornado Alley
Lakosztály 16"""
város = "East Centerville"
állapot = "KS"

[irodai cím]
utca = """123 Tornado Alley
Lakosztály 16"""
város = "East Centerville"
állapot = "KS"
```

A soron belüli táblázatokat kapcsos zárójelek ({}) veszik körül, és minden kulcs/érték pár vesszővel (,) van elválasztva.

``` toml
név = {első = "Tom", utolsó = "Pitt"}
```

## Hivatkozások ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

