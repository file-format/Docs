{
  "date" : "2019-10-11",
  "keywords" :[ "fișier tgs", "format fișier tgs", "ce este un fișier tgs", "fișier", "exemplu tgs", "extensie fișier tgs", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS – Format de fișier autocolant animat Telegram",
  "description":"Aflați despre formatul de fișier TGS și despre API-urile care pot crea și deschide fișiere TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Ce este un fișier TGS?

Un fișier cu extensia .tgs este un fișier autocolant animat care a fost introdus de serviciul de mesagerie multiplatformă, [Telegram](https://core.telegram.org/stickers#animated-stickers). Autocolantele animate sunt folosite de utilizatorii aplicațiilor de mesagerie pentru a trimite conținut mai îmbunătățit și mai plin de viață în mesaje, spre deosebire de grafica statică care sunt imagini statice. Telegram a folosit inițial formatul de fișier [WEBP](/ro/image/webp/) pentru autocolante cu imagini statice. Formatul de fișier TGS poate stoca date de animație la rezoluții mai mari și dimensiuni mai mici ale fișierului în comparație cu autocolantele statice WEBP. Fișierele TGS pot fi deschise folosind aplicații precum Telegram, 7-zip, Apple Archive Utility și Corel WinZip.

## Format de fișier TGS

Telegram a introdus formatul de fișier TGS încă din iulie 2019, pe baza bibliotecii Lottie. Un fișier TGS este format din text [JSON](/ro/web/json/) care este exportat dintr-o animație în Adobe After Effects. Textul JSON exportat este comprimat folosind compresia gzip care reduce dimensiunea fișierului. Informațiile JSON despre fișierul text sunt stocate într-un fișier text care devine baza ratelor ridicate de compresie.

### Specificații autocolante TGS

Formatul de fișier TGS impune anumite limitări pentru crearea autocolantelor animate TGS. Un fișier animat TGS:

* Dimensiunea autocolantului/pânzei trebuie să fie de 512×512 pixeli.
* Obiectele autocolante nu trebuie să părăsească pânza.
* Durata animației nu trebuie să depășească 3 secunde.
* Toate animațiile trebuie să fie redate în buclă.
* Dimensiunea autocolantului nu trebuie să depășească 64 KB după randare în Bodymovin.
* Toate animațiile trebuie să ruleze la 60 de cadre pe secundă.

### Exemplu de text JSON TGS

Un eșantion de autocolant animat, când este dezarhivat, conține următorul conținut de text JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referințe ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

