{
  "date": "2019-10-11",
  "keywords": [
"psb failu",
"psb faila formātā",
"kas ir psb fails",
"failu",
"psb piemērs",
"psb faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB — Photoshop lielais attēla faila formāts",
  "description": "Uzziniet par PSB failu formātu un API, kas var izveidot un atvērt PSB failus.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-lvb"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PSB fails?
Adobe Photoshop saglabā failus divos formātos. Faili, kuru izmērs ir 30 000 x 30 000 pikseļu, tiek saglabāti ar PSD paplašinājumu, un faili, kas ir lielāki par PSD, līdz pat 300 000 x 300 000 pikseļiem, tiek saglabāti ar PSB paplašinājumu, kas pazīstams kā Photoshop Big”. Konkrētāk, PSB faili var būt pat 4 EB (vairāk nekā 4,2 miljardi GB) ar attēliem, kuru augstums un platums ir līdz 300 000 pikseļu. No otras puses, PSD var būt līdz 2 GB un attēla izmēri var būt 30 000 pikseļi.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Informācija par faila formātu ##

Photoshop faila formāts ir sadalīts piecās galvenajās daļās ar daudziem garuma marķieriem, lai pārvietotos starp sadaļām.

|Faila formāts
---|
|Faila galvene
|Krāsu režīma dati
| Attēlu resursi
| Informācija par slāni un masku
|(((
Attēla dati
)))

### Faila galvene ###

Faila galvenē ir fiksēts 26 baitu garums, un tajā ir ietvertas attēla pamatīpašības.

BYTE paraksts [4] — vienāds ar '8BPS'.

WORD versija [2] — versijas numurs, PSD # 1, PSB # 2.

BYTE Reserved [6] — rezervēts un vienmēr nulle.

WORD Channels [2] — krāsu kanālu skaits attēlā, ieskaitot alfa kanālus. Tās vērtība svārstās no 1 līdz 56.

LONG Rows [4] — attēla augstums pikseļos, PSD 1-30 000, PSB 1-300 000.

LONG Columns [4] – attēla platums pikseļos, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] — bitu skaits kanālā. Atbalstītās vērtības ir 1,8,16 un 32.

WORD Mode [2] — faila krāsu režīms.

#### Režīma apraksts ####


|Mode|Apraksts
---|---|
|0|Bitkarte (vienkrāsaina)
|1|Pelēkā krāsā
|2|Indeksēts
|3|RGB
|4|CMYK
|7|Daudzkanālu
|8|Duotone (pustonis)
|9|Lab

### Krāsu režīma dati ###

Pēc faila galvenes sadaļas seko krāsu režīma datu sadaļa. Bloks sākas ar LONG numuru, kas norāda bloka garumu baitos. Krāsu režīma datu struktūra ir šāda:

4 baiti — šādu krāsu datu garums.

Mainīgs — krāsu dati

Ja režīma lauka vērtība galvenes sadaļā nav Indexed Color vai divtonis, bloka garums būs 0 un pēc garuma lauka datu nebūs.

Indeksētajiem krāsu attēliem garums būs 768 baiti, kas ietvers 256 krāsu paleti. Duotoni datos būs ekrāna parametri un cita saistīta informācija.

### Attēlu resursi ###

Pēc krāsu režīma datu sadaļas trešais bloks ir attēla resursu sadaļa. Pirmie četri baiti ir LONG skaitlis, kas norāda bloka garumu, kam seko resursu bloku sērija. Attēla resursu bloka struktūra ir šāda:

BYTE tips [4] — paraksts '8BIM

WORD ID [2] — attēla resursa ID. Ir saraksts ar resursu ID, ko var redzēt no atsauces saites.

BAYTE Name [Variable] — nosaukums: Pascal virkne ar vienmērīgu garumu. ***

LONG Size [4] — turpmāko resursu datu faktiskais lielums.

BAITU dati [Mainīgs} — resursa dati. Tas ir polsterēts, lai nodrošinātu vienmērīgu izmēru.

Tālāk ir īsi izskaidroti daži resursu formāti.

**Režģa un vadotņu resursa formāts:** Režģa un vadotņu informācija tiek glabāta resursu blokā. Šajos resursu blokos ir 16 baitu režģis un vadotnes galvene, kam seko 5 baitu ceļveža informācijas bloki.

**Sīktēlu resursa formāts:** Sīktēlu informācija tiek saglabāta attēla resursu blokā priekšskatījuma attēlošanai, kas sastāv no 28 baitu galvenes un JFIF sīktēla RGB formātā.

**Krāsu paraugu ņemšanas resursa formāts:** Krāsu paraugu ņemtāju informācija tiek saglabāta attēla resursu blokā ar 8 baitu galveni, kam seko mainīga garuma krāsu paraugu informācijas bloks.

### Slāņa un maskas informācija ###

Ceturtais bloks ir slāņu un masku informācijas bloks, un tajā ir informācija par slāņiem un maskām. Vispirms tiek saglabāta slāņa informācija un pēc tam maskas informācija.

**Slāņa informācija:** slāņa informācija sākas ar LONG vērtību, kas parāda slāņa informācijas garumu. Pēc tam ir WORD vērtību skaits, kas parāda slāņa ierakstu skaitu, kas jāievēro.

[8] – slāņu garums

[2] – slāņu skaits

[Mainīgs] — informācija par katru slāni.

[Mainīgs] — kanāla attēla dati.** **

**Maskas informācija:** Maskas struktūrai ir šāds formāts:


|Datu struktūra|Lauka nosaukums| Apraksts
---|---|---|
|VĀRDS| Pārklājuma krāsu telpa| (nav dokumentēts)
|BAITS[8]| Krāsu komponenti| 4x2 baitu krāsu komponenti
|VĀRDS| Necaurredzamība| 0#caurspīdīgs, 1#necaurspīdīgs
|BAITS| Laipns| 0#apgriezts, 1#aizsargāts, 128#izmantojiet saglabāto vērtību
|BAITS| polsterējums| iestatīts uz nulli

### Attēla dati ###

Pēdējā sadaļā ir attēla pikseļu dati. Attēla dati tiek saglabāti kā virkne secību plaknēs, ti, vispirms visi sarkanie dati, pēc tam visi zaļie dati utt. WORD katras rindas sākumā parāda izmēru baitos, kas saistīti ar katru skenēšanas līniju.

[2] – Saspiešanas metode:

[Mainīgs] — attēla dati plakanā secībā, piemēram, RRRR, GGGG, BBBB utt.

Saspiešanas metodes:

0 – Raw Attēla dati

1 — RLE saspiests

2 — rāvējslēdzējs bez paredzēšanas

3 — rāvējslēdzējs ar prognozi

## Atsauce Nr.

* [PSB faila formāts — Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB — Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


