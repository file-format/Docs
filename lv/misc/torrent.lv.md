{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent faila formāts - BitTorrent fails",
  "description":"Uzziniet par TORRENT failiem un API, kas var izveidot un atvērt TORRENT failus.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent-lv",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas ir TORRENT fails?

TORRENT fails ir teksta fails, ko BitTorrent un citas P2P (peer-to-peer) programmas izmanto satura lejupielādei un apmaiņai. Lejupielādējamais saturs var ietvert dokumentus, video, spēles, filmas un citus multivides materiālus, kas pieejami internetā. Tajā ir ietverta metadatu informācija par lejupielādējamā multivides saturu un atrašanās vietu. Programmatūra, piemēram, BitTorrent, datu lejupielādei izmanto informāciju no šī faila, piemēram, nosaukumu, faila lielumu un mapes struktūru. Torrent failus var pārvērst citos failu formātos, piemēram, [PDF](/pdf/) tiešsaistē.

## Kas ir Torrenting? TORRENT faila formāts datu apmaiņai

Torrentēšana ir datu failu apmaiņas (lejupielādes un augšupielādes) jēdziens, izmantojot BitTorrent tīklu. Atšķirībā no parastajiem serveriem, kur dati tiek augšupielādēti, lai citi varētu tiem piekļūt un lejupielādēt, torrent faili tiek izgūti un nosūtīti, izmantojot torrent tīklu. Kad lietotājs atver .torrent failu tādās lietojumprogrammās kā BitTorrent, programmatūra sāk lejupielādēt faila saturu bitu veidā. Ja vairākiem lietotājiem ir viens un tas pats fails, BitTorrent sadala lejupielādes starp visiem lietotājiem, lai paātrinātu lejupielādes procesu. Tajā pašā laikā tā lietotāja dators, kurš lejupielādē failu, kļūst arī par faila avotu, lai to nosūtītu citiem lietotājiem, kuri arī lejupielādē to pašu failu.

### TORRENT faila struktūra

Torrent fails ir failu saraksta un metadatu informācijas kombinācija par visām lejupielādējamā faila daļām. Tajā ir šāda informācija atslēgu veidā.

- announce — izsekotāja URL, kas tiek paziņots citiem vienaudžiem, lai informētu par faila pieejamību.
- Informācija — tiek kartēta uz vārdnīcu, kuras atslēgas ir atkarīgas no tā, vai tiek koplietots viens vai vairāki faili:
  - "faili — vārdnīcu saraksts, kas atbilst failam (tikai tad, ja tiek koplietoti vairāki faili). Katrā vārdnīcā ir šādi taustiņi:"
- `length` — faila lielums baitos.
- ceļš — virkņu saraksts, kas atbilst apakšdirektoriju nosaukumiem, no kuriem pēdējais ir faktiskais faila nosaukums
- garums — faila lielums baitos (tikai tad, ja tiek koplietots viens fails)
- `name` — faila nosaukums, kurā fails jāsaglabā
- gabala garums — baitu skaits vienā gabalā. Parasti tas ir 28 KiB = 256 KiB = 262 144 B.
- gabali — jaucējkodolu saraksts, kas ir katra gabala SHA-1 jaucējkoda savienojums.

## Vai Torrentēšana ir droša un likumīga?

Torrentēšanas protokols datu apmaiņai starp P2P lietotājiem ir drošs, jo tas ir tikai līdzeklis jebkura veida failu koplietošanai. Tādējādi pats protokols nav nedrošs vai nelikumīgs. Tomēr tīklā koplietotajā saturā var būt faili vai multivide, kas var pārkāpt kopīgoto dokumentu juridisko statusu. Šādā gadījumā šādu datu apmaiņa var izraisīt tiesiskas darbības pret pusēm, kas iesaistītas šādu failu publiskajā kopīgošanā.

## Atsauces

* [TORRENT fails — wikipedia](https://en.wikipedia.org/wiki/Torrent_file)


