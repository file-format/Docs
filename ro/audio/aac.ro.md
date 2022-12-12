{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "fișier", "extensie", "format", "Codare audio", "MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier AAC și despre API-urile care pot crea și deschide fișiere AAC.",
  "title" :"AAC – Fișier de codare audio avansată",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Ce este un fișier AAC?

AAC (Advanced Audio Coding) se referă la standardul de codare audio digitală care reprezintă fișiere audio bazate pe compresie audio cu pierderi. A fost lansat ca succesor al formatului de fișier **[MP3](/ro/audio/mp3/)** ținând cont că lateralul s-a confruntat cu probleme pentru implementarea de noi idei în procesul de codificare bazat pe dezvoltarea metodelor de comprimare a datelor. AAC realizează o calitate mai bună a sunetului în comparație cu MP3 la aceeași rată de biți. A fost definit în MPEG-2 Partea 7 (ISO/IEC 13818-7) și într-o formă actualizată în MPEG-4 Partea 3 (ISO/IEC 14496-3).

Formatul AAC a fost adoptat ca format media implicit de YouTube, iPhone, iPod, iPad, Apple iTunes și alte câteva platforme. Mai multe aplicații și API-uri sunt disponibile pentru conversia formatului de fișier AAC în alte formate, cum ar fi MP3, WMA, M4A, **[WAV](/ro/audio/wav/)** și altele.

### Scurt istoric al fișierului AAC

Formatul de fișier AAC este o versiune îmbunătățită a MP3, cu unele îmbunătățiri. Contribuit de mai multe companii, inclusiv Institutul Fraunhofer (Fraunhofer IIS - dezvoltatori de MP3), Nokia, Dolby, AT&T și Sony, formatul a fost declarat standard internațional de către Moving Picture Experts Group (MPEG) în aprilie 1997. Mai târziu, în 1999, MPEG-2 Partea 7 a fost actualizată și inclusă în familia de standarde MPEG-4. A fost cunoscut ca MPEG-4 Part 3, identificat ca ISO/IEC 14496-3: 1999 sau MPEG-4 Audio.

## Specificații de format de fișier AAC

Specificațiile de format de fișier AAC permit mai multă flexibilitate în proiectarea codecului decât MP3, rezultând mai multe strategii de codare simultane și o compresie eficientă. Formatul a fost selectat de o serie de platforme hardware pentru îmbunătățirile sale față de MP3 în ceea ce privește oferirea de suport pentru mai multe opțiuni chiar și la rate de biți mai mici. Specificațiile de format de fișier AAC sunt disponibile ca [MPEG-2 Partea 7](https://www.iso.org/standard/43345.html) și [MPEG-4 Partea 3](https://www.iso.org /standard/53943.html) (descărcare nu este gratuită). Formatul folosește următoarele tipuri de media:

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-generic

## AAC vs MP3 - Îmbunătățiri ##

Principalele diferențe dintre AAC și MP3 în ceea ce privește îmbunătățirile sunt următoarele:

* AAC acceptă o gamă mai largă de canale (până la 48) și rate de eșantionare (de la 8 kHz la 96 kHz)
* AAC are frecvențe de codare mai bune peste 16 kHz
* AAC are limite mai largi de variație în rezoluția frecvență-timp a unui banc de filtre care au condus la o codificare îmbunătățită a tranzitorilor și a părților staționare ale semnalului audio
* Banc de filtre mai eficient și mai simplu: un banc de filtre hibrid a fost înlocuit cu MDCT standard (transformată cosinus discretă modificată)
* Acceptă o eficiență îmbunătățită a compresiei folosind Tempral Noise Shaping (TNS), coeficienții de predicție ai timpului MDCT (predicție pe termen lung), stereo parametric, substituția de zgomot perceptiv, replicarea benzii spectrale (SBR).
* stereo mixt mai flexibil (se pot folosi diferite metode în diferite game de frecvență);

## Referințe ##

* [AAC - După Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

