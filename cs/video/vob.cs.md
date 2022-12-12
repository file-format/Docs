---
date: 2019-10-11
keywords: vob, .vob, formát souboru vob, formát souboru .vob, přípona .vob, přípona vob, formát videa vob, soubory DVD vob
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souborů VOB a rozhraních API, která mohou vytvářet a otevírat soubory VOB."
title: Formát souboru VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Co je soubor VOB? ##

Soubory VOB jsou obvykle uloženy v adresáři VIDEO_TS na disku DVD s příponou .vob. Soubory VOB obsahují video a audio data a také další data, jako jsou nabídky a titulky. VOB je založen na formátu programového toku MPEG-2, ale má další omezení a specifikace v soukromých tocích. Soubory VOB jsou striktní podmnožinou programových proudů MPEG, takže všechny soubory VOB jsou proudy programů MPEG, ale všechny programové proudy MPEG nejsou kompatibilní s VOB.

## Struktura DVD Video ##

Když je disk DVD otevřen na počítači, VIDEO_TS je adresář nejvyšší úrovně s AUDIO_TS. AUDIO_TS je prázdný a nepoužívá se. Uvnitř adresáře VIDEO_TS jsou soubory VOB, BUP a IFO. Soubory VOB obsahují obsah MPEG. Ty jsou rozděleny na části o velikosti 1 GB nebo méně, aby byly kompatibilní se všemi operačními systémy. Soubory IFO obsahují informace týkající se menu a struktury titulků. Soubory BUK jsou záložní soubory souborů IFO se stejným názvem. Tyto soubory jsou určeny k tomu, aby byly fyzicky uchovávány v samostatné oblasti, takže v případě poškození souboru IFO v důsledku fyzického poškození DVD může soubor BUK poskytnout stejné informace.

### Fyzické rozvržení ###

- Všechny soubory na disku musí být souvislé.
- Související soubory by měly být vedle sebe (VOB, IFO, BUP).
- Číslované soubory by měly být ve vzestupném pořadí.

## Ochrana proti kopírování ##

Mnoho video DVD je šifrováno a brání kopírování dat z DVD. K přehrávání souborů, které se nacházejí v nepřístupné vstupní oblasti disku DVD, jsou zapotřebí autentizační a dešifrovací klíče. Tyto klíče používá software pro dešifrování CSS, který je přítomen v přehrávači DVD nebo v softwarovém přehrávači. Bez klíčů nelze video soubory přehrát, protože klíče budou vyžadovány při otevření souborů.

## Reference ##

- [VOB - Wikipedie](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

