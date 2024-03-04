---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Luždirbti apie WEBM failo formatą ir API, kurios gali sukurti ir atidaryti WEBM failąs.
title: WEBM – WebM vaizdo failo formaat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Kas yra WEBM failas?

Failas su plėtiniu .webm yra vaizdo failas, pagrįstas atviru nemokamu WebM failo formatu. Jis skirtas dalytis vaizdo įrašais internete ir apibrėžia failų talpyklos struktūrą, įskaitant vaizdo ir garso formatus. WebM yra 100 % nemokama, įdiegiant aukštos kokybės atvirąsias technologijas, tokias kaip HTML, HTTP ir TCP/IP, kurias gali įdiegti visi. WebM buvo specialiai sukurtas teikti vaizdo įrašus žiniatinklyje, todėl jis optimizuotas srautiniam perdavimui su mažu skaičiavimo pėdsaku. Dėl to jis tinkamas vaizdo įrašams atkurti bet kuriame įrenginyje, ypač mažos galios nešiojamuosiuose kompiuteriuose, delniniuose kompiuteriuose ir planšetiniuose kompiuteriuose.

## WEBM failo formatas

WebM failo struktūra pagrįsta Matroska [MKV](/video/mkv/) sudėtinio rodinio failo formato poaibiu. Vaizdo įrašų srautai, esantys WebM faile, suglaudinami naudojant VP8 arba VP9 glaudinimo technologijas, kurios yra labai efektyvios. Panašiai, garso srautai WebM faile suglaudinami naudojant Vorbis arba Opus kodekus, kuriuos sukūrė [Xiph Foundation](https://www.xiph.org/). Visi šie vaizdo įrašai ir garso kodekai yra nemokami ir gali būti naudojami be jokių mokesčių.

Toliau pateikiamos apibendrintos WebM failo formato specifikacijos.

|Laukas|Aprašymas|
---|---|
|MIME tipo |vaizdo įrašas/webm|
|Tik garsas MIME tipo |garsas/webm|
|Vienodas tipo identifikatorius| org.webmproject.webm|
|Vaizdo įrašo kodeko pavadinimas| VP8 arba VP9|
|Garso kodeko pavadinimas| Vorbis arba Opus|

### WebM elementai

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Vardas |Aprašymas|
---|---|
|EBML|Nustatykite duomenų EBML charakteristikas, kurių reikia laikytis. Kiekvienas EBML dokumentas turi prasidėti šiuo.|
|EBMLVersion | EBML analizatoriaus versija, naudota kuriant failą.|
|EBMLReadVersion|Minimali EBML versija, kurią turi palaikyti analizatorius, kad galėtų skaityti šį failą.|
|EBMLMaxIDLength |Didžiausias ID, kurį rasite šiame faile, ilgis (4 ar mažiau Matroska).|
|EBMLMaxSizeLength|Didžiausias dydžių, kuriuos rasite šiame faile, ilgis (8 ar mažiau Matroska). Tai nepaiso elemento dydžio, nurodyto elemento pradžioje. Elementai, kurių nurodytas dydis yra didesnis nei leidžia EBMLMaxSizeLength, bus laikomi negaliojančiais.|
|DocType|Eilutė, apibūdinanti dokumento tipą, einančio po šia EBML antrašte (mūsų atveju webm).|
|DocTypeVersion|DocType interpretatoriaus versija, naudota kuriant failą.|
|DocTypeReadVersion|Minimali DocType versija, kurią turi palaikyti vertėjas, kad galėtų skaityti šį failą.|

#### Pasauliniai elementai

Šiuo metu palaikomas tik Void elementas, kuris naudojamas pažeistiems duomenims anuliuoti, kad būtų išvengta netikėto elgesio naudojant pažeistus duomenis. Turinys išmestas. Taip pat naudojamas rezervuoti vietą subelemente vėlesniam naudojimui.

#### Segmentas
Šiame elemente yra visi kiti aukščiausio lygio (1 lygio) elementai. Paprastai Matroska failą sudaro 1 segmentas.

#### Meta ieško informacijos

Palaikoma toliau nurodyta informacijos paieška.

|Elemento pavadinimas |Aprašymas|
---|---|
|SeekHead |Yra kito 1 lygio elemento padėtis.|
|Seek |Turi vieną paieškos įvestį į EBML elementą.|
|SeekID |Dvejetainis ID, atitinkantis elemento pavadinimą.|
|SeekPosition |Elemento padėtis segmente oktetais (0 = pirmasis 1 lygio elementas).|

## Nuorodos

* [WebM](https://www.webmproject.org/)

* [WebM kodų saugyklos](https://www.webmproject.org/code/#webp-repositories)


