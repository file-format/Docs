---
date: 2019-10-11
keywords: json, .json, formát souboru json, jak otevřít soubory json, zápis objektů javascript, formát dat json, formát souboru .json
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru JSON - Co je soubor JSON?
linktitle: JSON
description: "Přečtěte si o formátu souboru JSON a rozhraních API, která mohou vytvářet a otevírat soubory JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Co je soubor JSON?

JSON (JavaScript Object Notation) je otevřený standardní formát souboru pro sdílení dat, který k ukládání a přenosu dat používá text čitelný člověkem. Soubory JSON jsou uloženy s příponou .json. JSON vyžaduje méně formátování a je dobrou alternativou pro [XML](/cs/web/xml/). JSON je odvozen z JavaScriptu, ale je to datový formát nezávislý na jazyce. Generování a parsování JSON je podporováno mnoha moderními programovacími jazyky. *application/json* je typ média používaný pro JSON.

## Formát souboru JSON – Stručná historie

Byla potřeba komunikace mezi serverem a klientem v reálném čase, která vedla k vytvoření JSON. Formát JSON poprvé specifikoval Douglas Crockford v březnu 2001. JSON byl založen na standardu ECMA-262 3rd Edition – prosinec 1999, což je podmnožina JavaScriptu.

První vydání standardu JSON ECMA-404 bylo zveřejněno v říjnu 2013 společností Ecma International. RFC 7159 se stal hlavní referencí pro použití JSON na internetu v roce 2014. V listopadu 2017 byla publikována ISO/IEC 21778:2017 jako mezinárodní standard. RFC 8259 byl zveřejněn 13. prosince 2017 The Internet Engineering Task Force, což je aktuální verze internetového standardu STD 90.

## Struktura souborů JSON

Data JSON se zapisují v párech **klíč/hodnota**. Klíč a hodnota jsou odděleny dvojtečkou (:) uprostřed, přičemž klíč je vlevo a hodnota vpravo. Různé páry klíč/hodnota jsou odděleny čárkou(,). Klíč je řetězec ohraničený dvojitými uvozovkami, například "jméno". Hodnoty mohou být následujících typů.

- "Číslo".
- "Řetězec": Posloupnost znaků Unicode ohraničená dvojitými uvozovkami.
- `Boolean`: Pravda nebo nepravda.
- `Pole`: Seznam hodnot ohraničených například hranatými závorkami

```json
[ "Jablko", "Banán", "Pomeranč" ]
```

- `Object`: Sbírka párů klíč/hodnota obklopená například složenými závorkami

```json
{"name": "Jack", "age": 30, "favoriteSport" : "Fotbal"}
```

Objekty JSON lze také vnořit, aby reprezentovaly strukturu dat. Níže je uveden příklad objektu JSON.

### Příklad formátu JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Jaká je maximální velikost souboru JSON?

Maximální velikost souboru JSON není prakticky nijak omezena. Může být tak dlouhý, jak prostor vyžaduje uložený obsah.

Pokud jde o použití formátu souboru JSON pro přenos dat přes internet, je třeba dávat pozor na dostupné zdroje počítače. Pokud jsou přenášena velká data JSON, bude přenos ovlivněn, pokud má klientský prohlížeč omezenou paměť.


Neexistuje žádný pevný limit definovaný specifikací, ale musíte být opatrní, abyste nevyčerpali zdroje na počítačích vašich uživatelů, protože to rychle zhorší jejich uživatelskou zkušenost a pravděpodobně vaši aplikaci opustí.

## JSON vs XML

**XML** je další běžný a široce používaný formát souborů pro výměnu dat přes internet. Pokud jde o výměnu dat mezi aplikacemi, vývojáři mají možnost používat formáty souborů XML i JSON. JSON je však přijat jako nejpohodlnější způsob výměny dat mezi aplikacemi přes internet z následujících důvodů.

1. JSON poskytuje jasné a snáze čitelné zobrazení dat ve srovnání s formáty souborů XML
1. JSON snižuje režii přenosu dat přes internet, protože má menší počet znaků pro definování stejné sady dat ve srovnání s XML
1. Moderní programovací jazyky poskytují vestavěné analyzátory pro analýzu odezvy JSON přes web.

## Věděl jsi?

Můžete se stát přispěvatelem na FileFormat.com, aby komunita formátů souborů měla aktuální informace o vašich zjištěních. Pokud se chcete podělit o cokoli o formátech souborů JSON nebo Web, můžete svá zjištění zveřejnit v sekci [Zprávy o formátu webových souborů](https://news.fileformat.com/t/Web), kde se lidé o nich dozvědí více.

## Reference

- [JSON - Wikipedie](https://en.wikipedia.org/wiki/CSS)
– [Úvod do JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

