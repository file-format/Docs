{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "fișier", "extensie", "format", "format fișier de schimb audio", "muzică"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier WAV și despre API-urile care pot crea și deschide fișiere WAV.",
  "title" :"WAV – Format de fișier audio cu formă de undă",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Ce este un fișier WAV?

WAV, cunoscut pentru WAVE (Waveform Audio File Format), este un subset al specificației Microsoft Resource Interchange File Format (RIFF) pentru stocarea fișierelor audio digitale. Formatul nu aplică nicio compresie fluxului de biți și stochează înregistrările audio cu rate de eșantionare și rate de biți diferite. A fost și este unul dintre formatele standard pentru CD-uri audio. Fișierele Wave au dimensiuni mai mari în comparație cu noile formate de fișiere audio, cum ar fi [MP3](/ro/audio/mp3/), care utilizează compresia cu pierderi pentru a reduce dimensiunea fișierului, menținând în același timp aceeași calitate audio. Cu toate acestea, fișierele WAV pot fi comprimate folosind codecuri Audio Compression Manager (ACM). Există mai multe API-uri și aplicații disponibile care pot converti fișierele WAV în alte formate de fișiere audio populare.

**Știați?**
Puteți deveni colaborator la FileFormat.com pentru a menține comunitatea de format de fișier la curent cu descoperirile dvs. Dacă trebuie să împărtășiți ceva despre formatele de fișiere WAV sau audio, vă puteți publica concluziile în secțiunea [Știri despre format fișier audio](https://news.fileformat.com/t/audio), pentru ca oamenii să rămână la curent.

## Format fișier WAV ##

Formatul de fișier WAVE, fiind un subset al specificației Microsoft RIFF, începe cu un antet de fișier urmat de o secvență de fragmente de date. Un fișier WAVE are o singură bucată „WAVE” care constă din două sub-porțiuni:

* o bucată „fmt” - specifică formatul datelor
* o bucată de „date” - conține datele eșantionului real

### Antet fișier WAV ###

Antetul unui fișier WAV (RIFF) are o lungime de 44 de octeți și are următorul format:


|Poziții|Valoare eșantion|Descriere
---|---|---|
|1 - 4|"RIFF"|Marchează fișierul ca fișier riff. Caracterele au fiecare 1 octet.
|5 - 8|Dimensiunea fișierului (întreg)|Dimensiunea fișierului total - 8 octeți, în octeți (întreg de 32 de biți). De obicei, completați acest lucru după creare.
|9 -12|"WAVE"|Tip de fișier antet. Pentru scopurile noastre, este întotdeauna egal cu „WAVE”.
|13-16|"fmt "|Marcator de fragmente de format. Include trailing null
|17-20|16|Lungimea datelor de format așa cum este listată mai sus
|21-22|1|Tip de format (1 este PCM) - întreg de 2 octeți
|23-24|2|Număr de canale - întreg de 2 octeți
|25-28|44100|Rata de eșantionare - 32 de octeți întreg. Valorile comune sunt 44100 (CD), 48000 (DAT). Frecvența de eșantionare = Numărul de mostre pe secundă sau Hertzi.
|29-32|176400|(Rata de eșantionare * BitsPerSample * Canale) / 8.
|33-34|4|(BitsPerSample * Canale) / 8.1 - 8 biți mono2 - 8 biți stereo/16 biți mono4 - 16 biți stereo
|35-36|16|Biți per probă
|37-40|"date"|"date" bucată antet. Marchează începutul secțiunii de date.
|41-44|Dimensiunea fișierului (date)|Dimensiunea secțiunii de date.
|Valorile eșantionului sunt date mai sus pentru o sursă stereo pe 16 biți.

## Referințe ##

* [WAV - După Wikipedia](https://en.wikipedia.org/wiki/WAV)

