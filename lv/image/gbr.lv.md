{
  "date": "2019-10-11",
  "keywords": [
"gbr failu",
"gbr faila formātā",
"kas ir gbr fails",
"failu",
"gbr piemērs",
"gbr faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GBR faila formāts - Gerber faila formāts PCB",
  "description": "Uzziniet par GBR faila formātu un API, kas var izveidot un atvērt GBR failus.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gb-lvr"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GBR fails?

Fails ar paplašinājumu .gbr ir Gerber attēla faila formāts iespiedshēmas plates (PCB) dizaina datu apmaiņai. To izstrādāja Ucamco. PCB projektēšanas dati ir galvenā sastāvdaļa, kas apstrādes nozarei nepieciešama. GRB fails satur PCB datus, piemēram, vara slāņus, lodēšanas masku, leģendu un urbšanas un maršruta datus. To var izmantot, lai pārsūtītu datus, piemēram, PCB izgatavošanas raksturlielumus, tostarp biezumu vai apdari standartizētā formātā. Visas PCB projektēšanas sistēmas izvada Gerber failus, kurus var apstrādāt PCB ražošanas sistēmas. GBR faili tagad ir kļuvuši par de facto standartu iespiedshēmas plates (PCB) dizaina datu pārsūtīšanai. Ucamco ir nodrošinājis [free online viewer](https://gerber-viewer.ucamco.com/), lai atvērtu un skatītu GBR failu formātus.

## GBR faila formāts

GBR ir UTF-8 cilvēkiem lasāms formāts, kas sastāv tikai no 27 komandām. Šī īsā komandu saraksta un tā kompaktuma dēļ GBR ir viegli atkļūdot. Gerber pamatā ir atvērts vektora formāts 2D binārajiem attēliem. Metainformācija tiek pārsūtīta kopā ar attēliem, izmantojot atribūtus. Viens GRB fails norāda vienu attēlu, un tam nav jāinterpretē nekādi pievienotie faili vai ārējie parametri. Vienam attēlam ir nepieciešams tikai viens fails. Tas izmanto 7 bitu ASCII rakstzīmes visām komandām un nosaukumiem, kas definēti specifikācijā un ir drukājami. Tas pilnībā aptver pilnu attēla ģenerēšanu.

### GBR faila piemērs

Tālāk ir sniegts Gerber faila piemērs, kas izveido 1,5 mm diametra apli, kura centrā ir izcelsme. Katrā rindā ir viena komanda.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Atsauces

 * [Gerber formāts](https://www.ucamco.com/en/gerber)

