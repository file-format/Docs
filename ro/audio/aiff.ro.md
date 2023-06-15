{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "fișier", "extensie", "format", "format fișier de schimb audio", "muzică", "format fișier aiff", "aiff în mp3", "aiff vs wav", "conversie aiff în mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier AIFF și despre API-urile care pot crea, converti și deschide fișiere AIFF.",
  "title" :"AIFF - Format de fișier de schimb audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Ce este un fișier AIFF?
AIFF (Audio Interchange File Format) este un format de fișier audio necomprimat dezvoltat de Apple în 1998, dar se bazează pe **EA IFF 85** (Standard for Interchange Format Files dezvoltat de Electronic Arts), un format de wrapper utilizat pe sistemele Amiga . Acest format de fișier vine cu un standard pentru stocarea sunetelor eșantionate. Formatul este suficient de bun ca flexibilitate și permite stocarea sunetelor eșantionate mono sau multicanal la diferite rate de eșantionare și lățimi de eșantionare. Deoarece fișierele AIFF sunt necomprimate, acest lucru le face mai mari ca dimensiune decât alte formate cu pierderi, cum ar fi [MP3](/audio/mp3/).

Fișierele AIFF constau din 2 canale de audio stereo necomprimat cu dimensiunea eșantionului de 16 biți, înregistrate la 44,1 kHz. Datorită calității înalte a sunetului, un sunet de 5 minute poate ocupa până la 50 MB spațiu pe disc, care este similar cu formatul de fișier [WAV](/audio/wav/).

## AIFF vs WAV

AIFF și WAV sunt aproape aceleași din punct de vedere al calității. Ambele folosesc aceeași codare PCM (modulație cu cod de impulsuri), ceea ce le face mai mari ca dimensiune în comparație cu alte formate cu pierderi, cum ar fi [MP3](/audio/mp3/), [M4A](/audio/m4a/). Unele dintre diferențele generale sunt scrise în tabelul de mai jos:

|AIFF|WAV|
---|---|
|Folosit mai ales pentru MAC|Folosit mai ales pentru PC-uri|
|Permite metadeta| Nu permite metadeta|

## Structura fișierului AIFF

**EA IFF 85** stabilește o structură generală pentru stocarea datelor în fișiere. Un fișier **EA IFF 85** este format dintr-un număr de bucăți de date. O bucată este blocul de bază al fișierului AIFF constă din câteva informații de antet urmate de date:
{{< figure src="../chunk.png" alt="AIFF Chunk" >}}

Un fișier AIFF este o colecție de mai multe tipuri diferite de bucăți. Există două tipuri generale de bucăți care sunt importante pentru a forma o bucată de fișier AIFF:
- **Common Chunk**: Conține parametri importanți care descriu sunetul eșantionat, cum ar fi lungimea și rata de eșantionare.
- **Sound Data Chunk**: Conține mostrele audio reale.
Există multe alte bucăți opționale care listează parametrii instrumentului, definesc markeri, stochează informații specifice aplicației etc.

### Tipuri de bucăți locale

Tipurile de bucăți pentru a forma AIFF sunt date în tabelul de mai jos:

|Tip de bucată| Descriere|
---|---|
|Common Chunk|Common Chunk descrie parametrii fundamentali ai sunetului eșantionat|
|Sound Data Chunk|Sound Data Chunk conține cadrele eșantioane reale|
|Marker Chunk|Marker Chunk conține marcatori care indică pozițiile din datele de sunet|
|Instrument Chunk|Instrument Chunk definește parametrii de bază pe care un instrument, cum ar fi un sampler, i-ar putea folosi pentru a reda datele de sunet|
|MIDI Data Chunk|MIDI Data Chunk poate fi folosit pentru a stoca date MIDI|
|Secțiunea de înregistrare audio|Secțiunea de înregistrare audio conține informații relevante pentru dispozitivele de înregistrare audio|
|Aplicație Specific Chunk|Application Specific Chunk poate fi utilizat în orice scop de către producătorii de aplicații|
|Bucățiune de comentarii|Secțiunea de comentarii este folosită pentru a stoca comentarii în FORM AIFF|
|Fragmente de text - Nume, Autor, Drepturi de autor, Adnotare| Toate sunt fragmente de text|

## Referințe ##

* [Audio Interchange File Format - By Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

