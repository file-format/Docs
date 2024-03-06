{
  "date": "2021-06-09",
  "keywords": [
"bižele",
"failu",
"pagarinājumu",
"formātā",
"kas ir norādes fails",
"mūzika",
"cue faila formāts",
"cue faila formāta specifikācija",
"biželes lapa",
"CDRWIN"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CUE failu formātu un API, kas var izveidot, konvertēt un atvērt CUE failus.",
  "title": "CUE — Cue lapas fails",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-lve"
}
},
  "lastmod": "2021-07-01"
}

## Kas ir CUE fails?

Fails ar paplašinājumu .cue, kas pazīstams arī kā cue lapas fails, ir metadatu fails, kas satur informāciju par CD vai DVD ierakstu izkārtojumu. Tos atbalsta multivides atskaņotāji un optisko disku autorēšanas lietojumprogrammas. Uz galvenajiem kompaktdiskā saglabātajiem audio datiem ir atsauce uz norādes failu, kā arī ierakstu garuma, disku nosaukumu un izpildītāju specifikācijas. Tādējādi, ja vienā audio failā ir vairāki ieraksti, norādes failu var izmantot, lai sadalītu audio vairākos failos vai atsauktos uz dažādiem ierakstiem.

## CUE faila formāts

CUE vai cue lapas faili tiek glabāti vienkārša teksta formātā, kas ir cilvēkiem lasāms. Informācija norādes failā ir komandas ar vienu vai vairākiem parametriem. Šīs komandas attiecas vai nu uz visu failu, vai uz atsevišķu celiņu atkarībā no konkrētās komandas un konteksta. CDRWIN lietotāja rokasgrāmatā ir aprakstītas norāžu lapas sintakses un semantikas specifikācijas.

## CUE lapas būtiskās komandas

|Komanda|Apraksts|
---|---|
|FILE| Attiecas uz failu, kurā ir dati, un tā formātu, piemēram, [MP3](/audio/mp3/), [WAV](/audio/wav/) vai vienkāršu bināro diska attēlu)|
|TRACK| Definē ieraksta konteksta informāciju, piemēram, tā numuru un veidu vai režīmu.|
|INDEKSS| Apzīmē pozīciju kā indeksu FILE. Formāts ir mm:ss:ff (minūtes-sekundes kadrs).|
|PREGAP un POSTGAP|Tas norāda celiņa pirms vai pēcatstarpi, kas netiek saglabāta nevienā datu failā. Garums ir norādīts tādā pašā minūtēs-sekundes kadra formātā kā INDEX.|

### CUE lapas piemērs

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## Citi CUE faili

Tālāk ir norādīti citi failu tipi, kuros tiek izmantots faila paplašinājums **.cue**.

**Disks un multivide**
- [CUE — Cue lapas fails](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## Atsauces

* [.cda fails — Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


