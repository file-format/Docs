{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier WMV",
  "description":"Aflați despre formatul de fișier WMV și despre API-urile care pot crea și deschide fișiere WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Ce este un fișier WMV?

Advanced Systems Format (ASF) este un container multimedia digital conceput în principal pentru stocarea și transmiterea fluxurilor media. Microsoft Windows Media Video (WMV) este formatul video comprimat și Microsoft Windows Media Audio (WMA) este formatul audio comprimat împreună cu metadate suplimentare în containerul ASF dezvoltat de Microsoft. Odată ce fișierele WMV sau WMA sunt codificate cu codecuri Windows Media Video și Windows Media Audio, atunci acestea sunt reprezentate cu extensia .asf. WMV comprimă fișiere mari pentru o rată de transmisie mai bună într-o rețea, menținând în același timp calitatea videoclipului. WMV este special conceput pentru a rula pe toate dispozitivele Windows. După standardizarea de către Society of Motion Picture and Television Engineers (SMPTE), WMV este acum considerat a fi un format standard deschis.

## Istorie ##

Cu ajutorul codec-urilor proprietare Microsoft a fost dezvoltat în 1999 un nou format video comprimat, cunoscut sub numele de WMV7, care se baza pe MPEG-4 Partea 2. Au fost adăugate îmbunătățiri în alte două versiuni, adică WMV8 și 9. Microsoft a prezentat o versiune a 9^^^^ de WMV la SMPTE pentru standardizare în 2003, care a fost în cele din urmă standardizat în 2006 ca SMPTE 421M cunoscut și ca VC-1. Ideea din spatele WMV a fost să dezvolte un format media care să poată fi susținut de tot hardware-ul și software-ul suportat de Microsoft. Mai mult, un alt scop major a fost transmiterea fluxurilor video prin internet într-un scenariu optim. După standardizarea de la SMPTE, WMV a devenit și un format video pentru discuri Blu-ray.

## Specificații de format de fișier

### Container

În general, WMV este ambalat într-un container ASF, dar în plus, containerul Matroska sau AVI îl poate suporta și cu extensii de .mkv și respectiv .avi.

### Windows Media Video 9

Deși există diverse codecuri audio și video disponibile în seria Windows Media Video 9 pentru crearea și redarea de medii digitale, codecul WMV-9 este cel mai recent și cel mai bun codec video, deoarece poate obține compresia optimă de la rate de biți foarte mici, adică 160 x 120 la 10 Kbps la 1920 x 1080 la 4-8 Mbps pentru o varietate de videoclipuri HD.

### Structura Codecului

WMV-9 are un format intern de culoare pe 8 biți 4:2:0. La fel ca toate celelalte standarde populare de compresie video MPEG-1 și H.261, WMV-9 utilizează o schemă de compensare a mișcării și transformare spațială bazată pe bloc. În general, putem spune că aceste standarde efectuează compensarea mișcării bloc cu bloc din cadrul reconstruit anterior cu ajutorul unei mărimi 2-D numită vector de mișcare (MV) pentru a semnala deplasarea spațială. Blocul curent este format cu ajutorul predicției valorilor din cadrul reconstruit anterior de aceeași dimensiune care este deplasat de la poziția curentă de vectorul de mișcare. În cele din urmă, eroarea reziduală este calculată ca diferență între blocul prezis compensat cu mișcarea și blocul real. Această eroare reziduală este transformată folosind o transformare liniară de compactare a energiei, apoi cuantificată și codificată cu entropie.

Coeficienții de transformare cuantificați sunt decodați cu entropie, decuantificați și transformați invers pentru a produce o aproximare a erorii reziduale pe partea decodorului, care este apoi adăugată la predicția compensată de mișcare pentru a genera reconstrucția. Descrierea de nivel înalt a codecului este prezentată în imaginea următoare.

Restul secțiunii va discuta noile îmbunătățiri ale WMV-9 care îl diferențiază de restul soluțiilor de codare video, cum ar fi standardele MPEG. WMV-9 are cadre intra (I), prezise (P) și prezise bidirecționale (B). Cadrele intra sunt cele care sunt codificate independent și nu depind de alte cadre. Cadrele prezise sunt cadre care depind de un cadru din trecut. Decodificarea unui cadru prezis poate avea loc numai după ce au fost decodificate toate cadrele de referință anterioare cadrului curent începând de la cel mai recent cadru (I). Cadrele B sunt cadre care au două referințe - una în trecutul temporal și una în viitorul temporal. Cadrele B sunt transmise ulterior referințelor lor, ceea ce înseamnă că cadrele B sunt trimise în neregulă pentru a se asigura că referințele lor sunt disponibile în momentul decodării. Cadrele B în WMV-9 nu sunt folosite ca referință pentru cadrele ulterioare. Acest lucru plasează cadrele B în afara buclei de decodare, permițând să fie luate comenzi rapide în timpul decodării cadrelor B fără derive sau artefacte vizuale pe termen lung. Definiția de mai sus a cadrelor I, P și B este valabilă atât pentru secvențele progresive, cât și pentru secvențele întrețesute.

Performanța codecurilor video este comparată cu graficul lor de distorsiune a ratei (RD). Este o curbă 2-D care arată distorsiunea produsă de compresie la un anumit bitrate.

WMV-9 a rezolvat această problemă prin introducerea unei varietăți de tehnici enumerate mai jos:

1. Transformare adaptivă a dimensiunii blocului

2. Set de transformări de precizie limitată

3. Compensarea mișcării

4. Cuantificare și decuantizare

5. Codare avansată a entropiei

6. Filtrarea buclei

7. Codare avansată a cadrelor B

8. Codare interlace

9. Netezire prin suprapunere

10. Instrumente cu rată redusă

11. Compensarea decolorării

## Referințe ##

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html)
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


