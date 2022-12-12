{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "fișier", "extensie", "format", "Audio", "Global System for Mobile Audio", "extensie gsm", "fișiere gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier GSM și despre API-urile care pot crea și deschide fișiere GSM.",
  "title" :"GSM – Sistem global pentru format de fișier audio mobil",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Ce este un fișier GSM?

GSM este o extensie de fișier care este asociată cu Global System for Mobile Audio Format Files. Fișierele care conțin extensii GSM pot fi deschise pe platformele Linux, Windows și Mac OS. Formatul de fișier GSM aparține categoriei de fișiere audio.

Un fișier GSM este codificat cu un codec de compresie a sunetului CBR (constant bitrate) cu pierderi. Frecvența de eșantionare într-un fișier audio GSM este de 8000 de mostre/secundă, în timp ce rata de date este de aproximativ 13 kbps. Rata de biți din fișierele GSM asigură calitatea în timpul înregistrării vocii. Mai mult, formatul de fișier GSM este cunoscut și ca formatul standard global pentru a fi utilizat în telefoanele mobile și fișierele WAV pot fi, de asemenea, codificate cu ușurință folosind un format de fișier GSM. Orice problemă cu un fișier GSM poate fi rezolvată cu ușurință de către utilizator însuși, fără a merge la un expert.

De asemenea, utilizatorii pot converti fișierele GSM în formatele [MP3](/ro/audio/mp3/) și [MP4](/ro/audio/mp4/).

## Scurt istoric al formatului de fișier GSM

GSM este un format de fișier audio care a fost creat pentru telefonia prin internet în Europa. A fost dezvoltat de Institutul European de Standarde de Telecomunicații (ETSI) pentru a fi utilizat ca un celular digital 2G utilizat în telefoane mobile și tablete. Astăzi este folosit pentru a stoca înregistrări ale convorbirilor telefonice și ale mesajelor vocale.

## Specificații format fișier GSM ##

GSM funcționează pe o rețea structurată care constă din următoarele secțiuni:

- **Modulare** : Este un proces de transformare a datelor de intrare într-un format care poate fi transmis cu ușurință. Datele transmise sunt demodulate la capătul de recepție
- **Rata de transmisie**: GSM este un sistem digital care are o rată de biți de peste 270 kbps
- **Interval de frecvență Uplink**: 933-960 MHz
- **Interval de frecvență downlink**: 890 – 915 MHz
- **Spațierea canalelor**: înseamnă distanța dintre barierele adiacente care ar trebui să fie de aproximativ 200 kHz
- **Duplex Distance**: este spațiul dintre frecvențele uplink și downlink care ar trebui să fie de 80 MHz
- **Codificarea vorbirii**: GSM utilizează codarea predictivă liniară (LPC). LPC comprimă rata de biți. Când semnalul audio trece printr-un filtru și imită tractul vocal. GSM codifică vorbirea la 13 kbps

| Format de compresie audio | Algoritm | Rata de eșantionare | Transformarea ratei de biți | Latență | CBR | VBR | Stereo | Multicanal |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Da | Nu | Nu | Nu |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Da | Nu | Nu | Nu |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Da | Nu | Nu | Nu |

## Referințe ##

* [GSM - Prin Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

