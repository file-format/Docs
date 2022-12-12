---
date: 2019-10-11
keywords: rm, .rm, rm fájlformátum, .rm fájlformátum, .rm kiterjesztés, RealMedia fájlformátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az RM fájlformátumot és az API-kat, amelyek RM-fájlokat hozhatnak létre és nyithatnak meg."
title: RM fájlformátum
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Mi az RM fájl? ##

A RealMedia egy szabadalmaztatott multimédiás tárolóformátum, amelyet a RealNetworks fejlesztett ki, és amely az .rm kiterjesztést használja. A [RealAudio (RA)](/hu/audio/ra/) és a [RealVideo(RV)](/hu/video/rv/) kombinációjával használható az interneten keresztüli streameléshez. Ezek az adatfolyamok állandó bitrátájúak. A változó bitsebességhez a RealNetworks kifejlesztette a RealMedia Variable Bitrate (RMVB) formátumot. A RealMedia alkalmas tartalmak interneten keresztüli streamelésére, és például élő televíziózásra is használható.

## A ## RealMedia fájl szerkezete

A RealMedia fájl egy sor darabból áll, amelyek mindegyike a következő szerkezettel rendelkezik:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

A RealMedia fájlban a következő típusú darabok találhatók:

- **RealMedia fájlfejléc (.RMF)**: Ennek kell lennie a RealMedia fájl első darabjának. Egy fájlban csak egy RMF-darab található. Információkat tartalmaz a fejlécek számáról.
- **Fájltulajdonságok fejléc (PROP)**: Ez a RealMedia fájl általános tulajdonságairól tartalmaz információkat. Minden RealMedia fájlban csak egy ilyen típusú darab található.
- **Médiatulajdonságok fejléce (MDPR)**: Ez a csonk információkat tartalmaz az adatfolyam tulajdonságairól. Információkat tartalmaz az adatfolyam típusáról és a használt kodekről. A fájlban minden adatfolyamhoz tartozik egy MDPR-darab.
- **Tartalomleíró fejléc (CONT)**: Ez a rész olyan szöveges információkat tartalmaz, mint a RealMedia fájl tartalom címe vagy szerzője. Ez a rész csak tájékoztató jellegű.
- **Adatfejléc (DATA)**: Ez a csonk adatcsomagok csoportját tartalmazza.
- **Index fejléc (INDX)**: Ez a csonk az összes DATA csonk után jön, és indexbejegyzéseket tartalmaz. Egy fájl egynél több INDX-darabot tartalmazhat.

## Támogatott audio- és videoformátumok ##

### Hangformátumok ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- szakács: Főzni
- atrc: ATRAC3
- ralf: RealAudio veszteségmentes formátum
- raac: LC-AAC
- racp: HE-AAC

### Videóformátumok ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 prekurzor
- RV40: H.264 prekurzor, RV40
- RVTR: H.263+ (RV20)

## Hivatkozások ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

