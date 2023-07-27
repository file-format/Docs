{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Formát výměny materiálu",
  "keywords" :[ "MXF", "matroska video", "formát mkv", "jak přehrávat soubory MXF", "SMPTE", "multimédia", "video" ],
  "description":"Další informace o formátu souboru MXF a rozhraních API, která mohou vytvářet a otevírat soubory MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Co je soubor MXF?

Soubor s příponou .mxf je formát multimediálního kontejneru, který obsahuje digitální video a audio média spolu s metadatovými informacemi o souboru. Řídí se standardem SMPTE (Society of Motion Picture and Television Engineers), což je globální sdružení profesionálů z oblasti techniky, technologií a manažerů pracujících v mediálním a zábavním průmyslu. Soubory MXF lze převést do jiných formátů souborů, jako je [AVI](/cs/video/avi/) nebo [MOV](/cs/video/mov/).

## Formát souboru MXF

Soubory MXF jsou ve skutečnosti binární soubory, které se skládají ze sekvence bajtů v určitém formátu. Dekódovací aplikace musí být v souladu s tímto formátem, aby mu porozuměly a extrahovaly z něj informace. Formát umožňuje přidávat nové položky bez narušení zpětné kompatibility pomocí kódování KLV, které je popsáno níže.

* Klíč – identifikátor prvku, SMPTE Universal Label (UL)
* Délka – délka dat, což je kódování s proměnnou délkou použité za účelem snížení množství místa potřebného pro tuto položku
* Hodnota – skutečná hodnota prvku.

### Specifikace formátu SMPTE

Formát souboru MXF byl definován následujícími specifikacemi SMPTE.

* SMPTE ST 377-1:2011. Televize — Formát výměny materiálu (MXF) — Specifikace formátu souboru
* SMPTE ST 377-2 (nedokončená výroba k lednu 2012). Syntaxe rozšíření kódovaného KLV pro MXF.
* SMPTE ST 378:2004 (Archivováno 2010). Televize — Formát výměny materiálu (MXF) — Operační vzor 1a (jedna položka, jeden balíček)
* SMPTE ST 379-1:2009. Formát výměny materiálu (MXF) — MXF Generic Container
* SMPTE ST 379-2:2010. Formát výměny materiálu (MXF) -- MXF Constrained Generic Container
* SMPTE ST 380:2004. Televize — Formát výměny materiálu (MXF) — Schéma popisných metadat-1 (standardní, dynamické)
* SMPTE ST 381-1:2005. Televize — Formát výměny materiálu (MXF) — Mapování MPEG streamů do MXF Generic Container (Dynamic)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) – mapování MPEG streamů do MXF omezeného generického kontejneru
* SMPTE ST 382:2007. Material Exchange Format (MXF) – Mapování AES3 streamů a vysílání Wave Audio do MXF Generic Container
* SMPTE ST 383:2008. Televize — Formát výměny materiálu (MXF) — Mapování dat DV-DIF do generického kontejneru MXF
* SMPTE ST 384:2005. Televize — Formát výměny materiálu (MXF) — Mapování nekomprimovaných obrázků do generického kontejneru MXF
* SMPTE ST 385:2004. Televize — Formát výměny materiálu (MXF) — Mapování esence a metadat SDTI-CP do generického kontejneru MXF
* SMPTE ST 386:2004 (Archivováno 2010). Televize — Formát výměny materiálu (MXF) — Mapování dat Esence typu D-10 do generického kontejneru MXF
* SMPTE ST 387:2004 (Archivováno 2010). Televize — Formát výměny materiálu (MXF) — Mapování dat Esence typu D-11 do generického kontejneru MXF
* SMPTE ST 388:2004 (Archivováno 2010). Televize — Formát výměny materiálu (MXF) — Mapování A-law kódovaného zvuku do generického kontejneru MXF
* SMPTE ST 389:2005. Televize — Formát výměny materiálu (MXF) — MXF Generic Container Reverse Play System Element
* SMPTE ST 390:2011. Televize — Formát výměny materiálu (MXF) — Specializovaný operační vzor „Atom“ (zjednodušené znázornění jedné položky)
* SMPTE ST 391:2004 (Archivováno 2010). Televize — Formát výměny materiálu (MXF) — Operační vzor 1b (jedna položka, seskupené balíčky)
* SMPTE ST 392:2004. Televize — Formát výměny materiálu (MXF) — Operační vzor 2a (položky seznamu skladeb, jeden balíček)
* SMPTE ST 393:2004. Televize — Formát výměny materiálu (MXF) — Operační vzor 2b (položky seznamu skladeb, Ganged Packages)
* SMPTE ST 394:2006. Televize — Formát výměny materiálu (MXF) — Systémové schéma 1 pro generický kontejner MXF
* SMPTE ST 405:2006. Televize — Formát výměny materiálu (MXF) — Prvky a jednotlivé datové položky pro schéma obecného kontejnerového systému MXF 1
* SMPTE ST 407:2006. Televize — MXF — Provozní vzory 3a a 3b
* SMPTE ST 408:2006. Televize — MXF — Provozní vzory 1c, 2c a 3c
* SMPTE ST 410: 2008. Formát výměny materiálu – Generic Stream Partition.
* SMPTE ST 422:2006. Material Exchange Format — Mapování JPEG2000 Codestreams do MXF Generic Container
* SMPTE ST 429.4:2006. D-Cinema Packaging — Aplikace MXF JPEG 2000
* SMPTE ST 429.5:2006. D-Cinema Packaging — Timed Text Track File
* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption
* SMPTE ST 434:2006. Formát výměny materiálu — XML kódování pro metadata a informace o struktuře souborů
* SMPTE ST 436:2006. Televize — Mapování MXF pro linky VBI a doplňkové datové pakety
* SMPTE ST 2019-4:2009. Mapování VC-3 kódovacích jednotek do MXF Generic Container
* SMPTE ST 2037:2009. Mapování VC-1 do MXF Generic Container
* SMPTE RP 2008:2008. Formát výměny materiálu — Mapování toků AVC do generického kontejneru MXF
* SMPTE RP 2057:2011. Textový přenos metadat v MXF
* SMPTE EG 41:2004. Formát výměny materiálu (MXF) — Engineering Guideline. Poznámka: Tento dokument již nebyl uveden na webu SMPTE při konzultaci v lednu 2012.
* SMPTE EG 42:2004. Formát výměny materiálu (MXF) — popisná metadata MXF
* SMPTE RDD 3:2008. Specifikace interoperability e-VTR MXF
* SMPTE RDD 9-2009. Specifikace MXF interoperability produktů Sony MPEG Long GOP
* Nabídka tabulkového kalkulátoru registru metadat SMPTE.

### Strukturální metadata MXF

Strukturální metadata jsou v souboru MXF zásadní, protože obsahují užitečné informace o obsahu souboru. Metadata MXF obsahují informace, jako je snímková frekvence, velikost snímku, datum vytvoření souboru a vlastní datum úpravy. Strukturální metadata popisují strukturu a možnosti souboru MXF, který zahrnuje technický popis různých základních komponent a zprostředkování toho, jak je sestavena výstupní časová osa.

## Reference

* [MXF – Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF – Zpráva o pokroku](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Knihovna OpenSource C++ pro MXF](http://www.freemxf.org/)

