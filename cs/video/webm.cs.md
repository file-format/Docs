---
date: 2019-10-11
keywords: WEBM, Co je soubor WEBM, Formát souboru WEBM
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o formátu souborů WEBM a rozhraních API, která mohou vytvářet a otevírat soubory WEBM."
title: WEBM - WebM Video File Format
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Co je soubor WEBM?

Soubor s příponou .webm je soubor videa založený na otevřeném, bezplatném formátu souboru WebM. Byl navržen pro sdílení videa na webu a definuje strukturu kontejneru souborů včetně video a audio formátů. WebM je 100% zdarma, implementuje vysokou kvalitu založenou na otevřených technologiích, jako jsou HTML, HTTP a TCP/IP, které jsou otevřené komukoli k implementaci. WebM byl speciálně navržen pro poskytování videa na webu, díky čemuž je optimalizován pro streamování s nízkou výpočetní náročností. Díky tomu je vhodný pro přehrávání videí na jakémkoli zařízení, zejména na nízkoenergetických netboocích, kapesních počítačích a tabletech.

## Formát souboru WEBM

Struktura souborů WebM je založena na podmnožině formátu kontejnerového souboru Matroska [MKV](/cs/video/mkv/). Video streamy dostupné v souboru WebM jsou komprimovány pomocí kompresních technologií VP8 nebo VP9, které jsou vysoce účinné při kompresi. Podobně jsou audio streamy v souboru WebM komprimovány pomocí kodeků Vorbis nebo Opus, které byly vyvinuty [Xiph Foundation] (https://www.xiph.org/). Všechna tato videa a zvukové kodeky jsou zdarma a lze je používat bez jakýchkoli poplatků.

Níže jsou uvedeny souhrnné specifikace pro formát souboru WebM.

|Pole|Popis|
---|---|
|typ MIME |video/webm|
|Pouze zvuk MIME typu |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Název video kodeku| VP8 nebo VP9|
|Název zvukového kodeku| Vorbis nebo Opus|

### Prvky WebM

WebM, který je podmnožinou specifikací Matrosky, poskytuje podporu pro některé funkce Matrosky. Následuje popis podporovaných prvků.

#### EBML

|Jméno |Popis|
---|---|
|EBML|Nastavit charakteristiky EBML dat, která se mají dodržovat. Každý dokument EBML musí začínat tímto.|
|EBMLVersion |Verze analyzátoru EBML použitého k vytvoření souboru.|
|EBMLReadVersion|Minimální verze EBML, kterou musí analyzátor podporovat pro čtení tohoto souboru.|
|EBMLMaxIDLength |Maximální délka ID, která najdete v tomto souboru (4 nebo méně v Matrosce).|
|EBMLMaxSizeLength|Maximální délka velikostí, které najdete v tomto souboru (8 nebo méně v Matrosce). Toto nepřepíše velikost prvku uvedenou na začátku prvku. Prvky, které mají uvedenou velikost větší než povolená EBMLMaxSizeLength, budou považovány za neplatné.|
|DocType|Řetězec, který popisuje typ dokumentu, který následuje za touto hlavičkou EBML (v našem případě "webm").|
|DocTypeVersion|Verze překladače DocType použitého k vytvoření souboru.|
|DocTypeReadVersion|Minimální verze DocType, kterou musí interpret podporovat, aby mohl číst tento soubor.|

#### Globální prvky

V tuto chvíli je podporován pouze prvek `Void`, který se používá k vymazání poškozených dat, aby se zabránilo neočekávanému chování při použití poškozených dat. Obsah je zahozen. Používá se také k rezervaci místa v dílčím prvku pro pozdější použití.

#### Segment
Tento prvek obsahuje všechny ostatní prvky nejvyšší úrovně (úroveň 1). Soubor Matroska se obvykle skládá z 1 segmentu.

#### Informace o hledání metadat

Podporovány jsou následující informace pro vyhledávání.

|Název prvku |Popis|
---|---|
|SeekHead |Obsahuje pozici dalšího prvku úrovně 1.|
|Seek |Obsahuje jeden záznam hledání prvku EBML.|
|SeekID |Binární ID odpovídající názvu prvku.|
|SeekPosition |Pozice prvku v segmentu v oktetech (0 = prvek první úrovně 1).|

## Reference

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)

