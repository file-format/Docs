{
  "date": "2019-10-11",
  "keywords": [
"tgs failu",
"tgs faila formātā",
"kas ir tgs fails",
"failu",
"tgs piemērs",
"tgs faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGS — telegrammas animācijas uzlīmes faila formāts",
  "description": "Uzziniet par TGS faila formātu un API, kas var izveidot un atvērt TGS failus.",
  "linktitle": "TGS",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-lvs"
}
},
  "lastmod": "2021-04-02"
}

## Kas ir TGS fails?

Fails ar paplašinājumu .tgs ir animēts uzlīmes fails, ko ieviesa starpplatformu ziņojumapmaiņas pakalpojums [Telegram](https://core.telegram.org/stickers#animated-stickers). Ziņojumapmaiņas lietotņu lietotāji izmanto animētas uzlīmes, lai ziņojumos nosūtītu uzlabotu un dzīvīgāku saturu atšķirībā no statiskās grafikas, kas ir nekustīgi attēli. Telegram sākotnēji izmantoja [WEBP](/image/webp/) faila formātu nekustīgu attēlu uzlīmēm. TGS faila formāts var saglabāt animācijas datus ar augstāku izšķirtspēju un mazāku faila izmēru, salīdzinot ar statiskajām WEBP uzlīmēm. TGS failus var atvērt, izmantojot tādas lietojumprogrammas kā Telegram, 7-zip, Apple Archive Utility un Corel WinZip.

## TGS faila formāts

Telegram TGS faila formātu ieviesa jau 2019. gada jūlijā, pamatojoties uz Lottie bibliotēku. TGS fails sastāv no [JSON](/web/json/) teksta, kas tiek eksportēts no animācijas programmā Adobe After Effects. Eksportētais JSON teksts tiek saspiests, izmantojot gzip saspiešanu, kas samazina faila lielumu. JSON informācija par teksta failu tiek glabāta teksta failā, kas kļūst par pamatu augstam saspiešanas līmenim.

### TGS uzlīmju specifikācijas

TGS faila formāts uzliek noteiktus ierobežojumus TGS animēto uzlīmju izveidei. TGS animēts fails:

 * Uzlīmes/audekla izmēram jābūt 512x512 pikseļiem.
 * Uzlīmju priekšmeti nedrīkst atstāt audeklu.
 * Animācijas ilgums nedrīkst pārsniegt 3 sekundes.
 * Visām animācijām jābūt cilpām.
 * Uzlīmes izmērs pēc atveidošanas programmā Bodymovin nedrīkst pārsniegt 64 KB.
 * Visām animācijām ir jādarbojas ar ātrumu 60 kadri sekundē.

### TGS JSON teksta paraugs

Animētas uzlīmes paraugā, kad tas ir izspiests, ir šāds JSON teksta saturs.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Atsauces Nr.

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip — Wikipedia](https://en.wikipedia.org/wiki/Gzip)


