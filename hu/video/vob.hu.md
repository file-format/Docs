---
date: 2019-10-11
keywords: vob, .vob, vob fájlformátum, .vob fájlformátum, .vob kiterjesztése, vob kiterjesztése, vob videó formátuma, vob dvd fájlok
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg a VOB fájlformátumot és az API-kat, amelyek VOB-fájlokat hozhatnak létre és nyithatnak meg."
title: VOB fájl formátum
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Mi az a VOB fájl? ##

A VOB-fájlok általában a VIDEO_TS könyvtárban tárolódnak egy .vob kiterjesztésű DVD-lemezen. A VOB fájlok videó- és hangadatokat, valamint egyéb adatokat, például menüket és feliratokat tartalmaznak. A VOB MPEG-2 programfolyam formátumon alapul, de további korlátozásokkal és specifikációkkal rendelkezik a privát adatfolyamokban. A VOB fájlok az MPEG programfolyamok szigorú részhalmazát képezik, így minden VOB fájl MPEG programfolyam, de az MPEG programfolyamok nem VOB-kompatibilisek.

## A DVD videó felépítése ##

Amikor egy DVD-lemezt megnyit a számítógépen, a VIDEO_TS az AUDIO_TS legfelső szintű könyvtára. Az AUDIO_TS üres és nincs használatban. A VIDEO_TS könyvtárban VOB, BUP és IFO fájlok találhatók. A VOB fájlok MPEG tartalmat tartalmaznak. Ezek 1 GB-os vagy kisebb méretű darabokra vannak felosztva, hogy kompatibilisek legyenek az összes operációs rendszerrel. Az IFO fájlok a menükre és a címszerkezetre vonatkozó információkat tartalmaznak. A BUK-fájlok az azonos nevű IFO-fájlok biztonsági másolatai. Ezeket a fájlokat fizikailag külön területen kell tárolni, így abban az esetben, ha az IFO fájl a DVD fizikai sérülése miatt megsérül, a BUK fájl ugyanazt az információt nyújthatja.

### Fizikai elrendezés ###

- A lemezen lévő összes fájlnak egybefüggőnek kell lennie.
- A kapcsolódó fájlok egymás mellett legyenek (VOB, IFO, BUP).
- A számozott fájlok növekvő sorrendben legyenek.

## Másolásvédelem ##

Sok videó DVD titkosított, és megakadályozza az adatok másolását a DVD-ről. A DVD elérhetetlen bevezető területén található fájlok lejátszásához hitelesítési és visszafejtési kulcsokra van szükség. Ezeket a kulcsokat a DVD-lejátszóban vagy a szoftverlejátszóban található CSS visszafejtő szoftver használja. A gombok nélkül a videofájlok nem játszhatók le, mivel a fájlok megnyitásakor a rendszer kérni fogja a gombokat.

## Hivatkozások ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

