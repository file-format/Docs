{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML - E-mail-besked",
  "description": "Lær om EML filformat og API'er, der kan oprette og åbne EML filer.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-dal"
}
},
  "lastmod": "2019-09-16"
}

## Hvad er en EML fil?

EML-filformat repræsenterer e-mail-beskeder gemt ved hjælp af Outlook og andre relevante applikationer. Næsten alle e-mail-klienter understøtter dette filformat for dets overensstemmelse med RFC-822 Internet Message Format Standard. Microsoft Outlook er standardsoftwaren til at åbne EML-meddelelsestyper. EML-filer kan bruges til at gemme på disk samt til at sende ud til modtagere ved hjælp af kommunikationsprotokoller.

## Kort historie om EML

EML-filformatspecifikationer er tilgængelige i henhold til [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) standardformat. Før RFC-822 styrede RFC-733 reglerne for udveksling af netværksmeddelelser, indtil førstnævnte i 1982 blev skabt som en forbedring af lateral ved at etablere ARPA-standarder. Samtidig skabte Microsoft sine egne COM-moduler til udvikling af sin egen e-mail-klient, dvs. Outlook Express. RFC-822 tog vejen til at blive etableret som et proprietært format, da Microsoft afveg fra den åbne standard og skabte [PST](/email/pst/) filformat, hvor e-mails gemmes i et meget struktureret databaseformat. Dette resulterede i problemer for brugere af ikke-Microsoft e-mail-klienter, når e-mails blev videresendt fra Microsoft Outlook.

Det var i 2001, da 822-standarden blev forbedret til 2822 - Internet Message Format, som i øjeblikket bruges til at oprette, læse og sende EML-meddelelser i MIME RFC-822-format.

## EML filformatspecifikationer

EML-filer består af to adskilte sektioner:

* **Overskrifter** - Indeholder oplysninger om meddelelseshoved

* **Meddelelsestekst** - Indeholder en række oplysninger, der kan omfatte beskedindhold, indlejrede billeder og vedhæftede filer


### Oplysninger om overskrifter ###

En EML-fil består af headers-oplysninger og eventuelt beskedtekst. Hver overskriftslinje i EML'en har to dele adskilt af et kolon :. Den første kaldes Header Name, og den efter kolon er header body. Sådanne overskrifter inkluderer f.eks.:

* Afsender e-mailadresse

* Modtagerens e-mailadresse

* Emne for e-mail

* Tids- og datostempel for besked


**Eksempel på overskrift**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Meddelelsestekst ###

EML-meddelelsesteksten indeholder den primære information om e-mail i form af tekst, hyperlinks og vedhæftede filer. E-mail-brødtekst kan indeholde almindelig læsbar tekst, men det er ikke nødvendigt. I dette tilfælde kan meddelelsesteksten være tom eller indeholde kodede vedhæftede filer.

Indholdet af meddelelsesteksten er beskrevet af dens indholdstype, som gør det muligt for læseapplikationerne at læse informationen i de respektive formater. Det repræsenterer faktisk arten og formatet af et dokument. Strukturen af en MIME-type eller indholdstype er meget enkel; den består af en type og en undertype, to strenge, adskilt af et '/'. Ingen plads er tilladt. Typen repræsenterer kategorien og kan være en diskret eller en flerdelt type. Undertypen er specifik for hver type. Listen over typer, der falder i kategorien Content-Type, er lang, men nogle vigtige indholdstyper er som følger:


|**Type**|**Beskrivelse**|**Eksempel på undertyper**
---|---|---|
|tekst|Repræsenterer format, der kan læses af mennesker|text/plain, text/html, text/css, text/javascript
|image|Repræsenterer billede af enhver type undtagen videoer|image/bmp, image/png, image/jpg, image/gif
|audio|Repræsenterer ethvert lydfilformat|audio/mdi, audio/wav
|application|Repræsenterer enhver form for binære data|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Repræsentation af tilknytning i EML Body

EML body indeholder grænser for hver indholdstype, den indeholder. Vedhæftet fil i meddelelsesteksten identificeres ved dets indholdstype og indholdsdisposition som vist i følgende eksempel:

Indholdstype: tekst/almindelig; tegnsæt#windows-1252; navn#apple app store.txt
Indhold-Disposition: vedhæftet fil; filnavn#apple app store.txt
Indholdsoverførselskodning: base64
X-Attachment-Id: f_jkhztmd02

Som det kan ses, gør Content-Disposition indstillet til vedhæftet fil det muligt for læseapplikationerne at få vedhæftede oplysninger såsom vedhæftningsfilnavn og overførselskodning. Vedhæftningshovedoplysninger efterfølges af kodet vedhæftede indhold, der skal læses.

#### Eksempel på regneark som vedhæftet fil

Indholdstype: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; navn#english_spodr.xlsx
Indhold-Disposition: vedhæftet fil; filnavn#english_spodr.xlsx
Indholdsoverførselskodning: base64
X-Attachment-Id: f_jkhztmd43

## Hvordan man åbner en EML fil

Du kan åbne EML filer ved hjælp af forskellige e-mail-programmer såsom:

 * **Apple Mail på macOS**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

EML-filer gemmes i almindeligt tekstformat, og du kan også åbne disse EML-filer med populære teksteditorer såsom **TextEdit** på macOS og **Microsoft Notepad** på Windows OS.

## Sådan konverteres en EML-fil

Du kan konvertere EML-filer til flere andre formater med programmer som Apple Mail og Microsoft Outlook.

For eksempel kan Microsoft Outlook konvertere EML-fil til følgende formater:

**[.MSG](/eml/msg/)** - Microsoft Outlook-meddelelsesformat
**[.PDF](/pdf/)** - Protable Document Format

## Referencer

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


