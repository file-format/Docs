{
"data": "2023-08-03",
  "keywords": [
"usr",
"fișier usr",
"Ce este un fișier usr",
"cum se deschide fișierul usr",
"fişier",
"extensie fișier usr",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format fișier USR - Fișier de date GPS Lowrance",
  "description":"Aflați despre formatul USR și despre API-urile care pot crea și deschide fișiere USR.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Ce este un fișier USR?

Extensia de fișier ".usr" este, de asemenea, legată de dispozitivele GPS Lowrance. În special, este utilizat pentru stocarea datelor GPS într-un format cunoscut sub numele de "Format de date utilizator" (format USR), care este utilizat de dispozitivele GPS Lowrance.

Când utilizați o unitate GPS Lowrance, vă puteți salva punctele de trecere, traseele și rutele ca fișiere ".usr". Aceste fișiere conțin de obicei informații precum latitudinea, longitudinea, altitudinea, marcajul de timp și alte date legate de activitățile dvs. GPS.

Iată câteva utilizări comune ale fișierelor .usr cu dispozitivele GPS Lowrance:

- **Waypoints:** Waypoints sunt locații specifice marcate pe GPS, cum ar fi repere, locuri de pescuit preferate sau puncte de interes. Puteți salva aceste locații ca fișiere .usr și pot fi importate, exportate sau partajate cu alți utilizatori Lowrance GPS.

- **Track:** Tracks reprezintă calea înregistrată a mișcărilor tale GPS. Puteți salva jurnalele de traseu ca fișiere .usr, permițându-vă să revizuiți și să analizați rutele mai târziu sau să le partajați altora.

- **Rute:** Rutele sunt căi predefinite pe care le puteți crea și salva pe dispozitivul GPS. Aceste rute pot fi salvate și ca fișiere .usr pentru utilizare sau partajare viitoare.

Pentru a gestiona fișierele .usr de pe dispozitivul dvs. GPS Lowrance, utilizați de obicei software precum "Insight Planner" sau "Lowrance GPS Utility" de la Lowrance pentru a importa, exporta și manipula datele GPS.

## Format de fișier USR - Mai multe informații

În dispozitivele GPS Lowrance iFinder, fișierele .usr sunt create și salvate pe cardul de memorie MultiMediaCard (MMC) introdus în dispozitiv. Aceste fișiere conțin date despre utilizator, cum ar fi puncte de referință, trasee și rute.

Pentru a transfera fișierele .usr de pe MMC pe un computer, puteți urma acești pași:

- **Scoateți MMC:** Scoateți cu atenție MultiMediaCard (MMC) de pe dispozitivul GPS Lowrance iFinder.

- **Inserați MMC în computer:** Folosiți un cititor de carduri MMC adecvat pentru a introduce cardul de memorie în slotul pentru cititorul de carduri al computerului.

- **Găsiți fișiere .usr:** Odată ce MMC este recunoscut de computerul dvs., ar trebui să puteți accesa fișierele stocate pe acesta. Căutați fișierele .usr, care conțin datele dvs. GPS.

- **Conversie cu GPSBabel:** Pentru a converti fișierele .usr într-un alt format GPS, puteți utiliza GPSBabel, care este un instrument gratuit și open-source pentru a lucra cu diferite formate de fișiere GPS. GPSBabel acceptă o gamă largă de formate de intrare și ieșire, permițându-vă să convertiți fișierele .usr în formate compatibile cu alte software-uri sau dispozitive GPS.

Puteți descărca GPSBabel de pe site-ul oficial (http://www.gpsbabel.org/) și îl puteți instala pe computer. Odată instalat, puteți utiliza interfața de linie de comandă a software-ului sau interfața grafică cu utilizatorul (dacă este disponibilă) pentru a efectua conversia.

De exemplu, dacă doriți să convertiți fișierele .usr în format GPX, puteți utiliza o comandă precum:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Comanda de mai sus îi cere GPSBabel să citească fișierul de intrare "input.usr" în format Lowrance USR și să scrie fișierul de ieșire "output.gpx" în format GPX.

- **Importarea/Folosirea fișierelor convertite:** După conversie, veți avea datele dvs. GPS în noul format (de exemplu, GPX), pe care îl puteți utiliza cu alte software-uri sau dispozitive GPS care acceptă acel format.

## Cum se deschide fișierul USR?

Programele care deschid sau fac referire la fișiere USR includ

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referințe
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

