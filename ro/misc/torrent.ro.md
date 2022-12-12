{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier torrent - fișier BitTorrent",
  "description":"Aflați despre fișierele TORRENT și API-urile care pot crea și deschide fișiere TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Ce este un fișier TORRENT?

Un fișier TORRENT este un fișier text care este utilizat de BitTorrent și alte programe P2P (peer-to-peer) pentru descărcarea și schimbul de conținut. Conținutul descărcabil poate include documente, videoclipuri, jocuri, filme și alte media disponibile pe internet. Include informații despre metadate despre conținutul și locația suportului media care urmează să fie descărcat. Software precum BitTorrent utilizează informații din acest fișier, cum ar fi numele, dimensiunea fișierului și structura folderului pentru descărcarea datelor. Fișierele torrent pot fi convertite în alte formate de fișiere, cum ar fi [PDF](/ro/pdf/) online.

## Ce este torrentul? Formatul de fișier TORRENT pentru schimbul de date

Torrentul este conceptul de schimb (descărcare și încărcare) de fișiere de date folosind rețeaua BitTorrent. Spre deosebire de serverele convenționale în care datele sunt încărcate pentru ca alții să le acceseze și să le descarce, fișierele torrent sunt preluate și trimise folosind rețeaua torrent. Când un utilizator deschide un fișier .torrent în aplicații precum BitTorrent, software-ul începe să descarce conținutul fișierului pe biți. Dacă mai mulți utilizatori au același fișier, BitTorrent împarte descărcările între toți utilizatorii pentru a accelera procesul de descărcare. În același timp, computerul utilizatorului care descarcă fișierul devine și sursa fișierului pentru trimiterea acestuia către alți utilizatori care descarcă și ei același fișier.

### Structura unui fișier TORRENT

Un fișier torrent este o combinație de o listă de fișiere și informații despre metadate despre toate părțile fișierului care urmează să fie descărcate. Conține următoarele informații sub formă de chei.

- `announce` — URL-ul trackerului care este anunțat altor colegi pentru informarea despre disponibilitatea fișierului
- `info` — Aceasta se mapează la un dicționar ale cărui chei depind de faptul că unul sau mai multe fișiere sunt partajate:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — dimensiunea fișierului în octeți.
- `cale` — o listă de șiruri de caractere corespunzătoare numelor subdirectoarelor, ultimul dintre acestea fiind numele real al fișierului
- `length` — dimensiunea fișierului în octeți (doar atunci când un fișier este partajat)
- `name` — numele fișierului în care urmează să fie salvat fișierul
- `lungimea piesei` — numărul de octeți pe bucată. Acesta este de obicei 28 KiB = 256 KiB = 262.144 B.
- `pieces` — o listă hash care este o concatenare a hash-ului SHA-1 al fiecărei piese.

## Torrentul este sigur și legal?

Protocolul de torrenting pentru schimbul de date între utilizatorii P2P este sigur, deoarece este doar mijlocul de partajare a oricărui tip de fișier. Astfel, protocolul în sine nu este nesigur sau ilegal. Cu toate acestea, conținutul partajat prin intermediul rețelei poate conține fișiere sau medii care pot încălca statutul juridic al documentelor partajate. În acest caz, schimbul de astfel de date poate provoca acțiuni legale împotriva părților implicate în partajarea publică a unor astfel de fișiere.

## Referințe

* [Fișier TORRENT - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

