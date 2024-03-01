{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE-tiedosto - Mikä on .gcode-tiedosto ja miten se avataan?",
   "description":"Lisätietoja GCODE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GCODE-tiedostoja.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-fi",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Mikä on GCODE-tiedosto?

**GCODE-tiedosto** on pelkkä tekstitiedosto, joka sisältää ohjeet tietokoneistettujen työstökoneiden ja 3D-tulostimien ohjaamiseen. G-koodi tai geometrinen koodi on kieli, jota käytetään ohjaamaan **CNC (Computer Numerical Control)** -koneiden liikkeitä ja toimintoja. CNC-koneita ovat jyrsinkoneet, sorvit, reitittimet ja 3D-tulostimet.

G-koodikomennot kirjoitetaan tietyllä syntaksilla, joka koostuu tyypillisesti kirjaimista ja numeroista; jokainen komento ohjaa konetta suorittamaan tiettyjä toimia, kuten siirtämään työkalua tiettyyn asentoon, vaihtamaan työkalua tai säätämään nopeutta.

G-koodi luodaan usein **CAM (Computer-Aided Manufacturing)** -ohjelmistolla; CAM-ohjelmisto ottaa 3D-mallin tai 2D-suunnittelun ja luo vastaavat työstöradat ja G-koodikäskyt; G-kooditiedosto ladataan sitten CNC-koneeseen tai 3D-tulostimeen suorittamista varten.

G-kooditiedostoilla on yleensä tiedostotunniste .nc tai .gcode, esimerkiksi program.nc tai print.gcode.

## GCODE-tiedostorakenne:

GCODE-tiedostot ovat pelkkiä tekstitiedostoja, joiden jokainen rivi sisältää tietyn komennon; nämä komennot vaihtelevat koneen liikkeen ohjaamisesta lämpötilan, nopeuden ja muiden esineen valmistuksen kannalta olennaisten parametrien säätämiseen.

GCODE:n syntaksi sisältää kirjainten ja numeroiden yhdistelmän; kukin edustaa erillistä toimintaa tai parametria; yleisiä komentoja ovat G0 ja G1 liikettä varten, M3 ja M5 karan ohjauksille ja S ja F nopeuden ja syöttöarvon säädöille.

## GCODE-sukupolvi:

Viipalointiohjelmistot, kuten **Simplify3D** ja **Slic3r**, kääntävät tietokoneavusteisen suunnittelun (CAD) piirustukset GCODE:ksi; CAD-ohjelmistoa käytetään luomaan 3D-malleja, jotka sitten viedään muodossa, kuten STL; viipalointiohjelmisto ottaa nämä mallit ja luo GCODE-tiedoston, jossa määritellään yksityiskohdat, kuten kerroksen korkeus, tulostusnopeus ja lämpötila-asetukset.

## GCODE esimerkki

Tässä on yksinkertainen esimerkki G-koodista CNC-koneen siirtämiseen:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Kuinka avata GCODE -tiedosto?

G-kooditiedoston avaamiseen voit käyttää erilaisia ohjelmistoja tarpeidesi mukaan.

Jos loit G-koodin 3D-tulostimelle; voit avata sen 3D-tulostimesi mukana tulleella ohjelmistolla tai erillisellä viipalointiohjelmistolla; esimerkkejä ovat **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** tai **Repetier-Host**; Näissä ohjelmissa on usein käyttäjäystävällinen käyttöliittymä, jonka avulla voit ladata ja visualisoida G-koodia.

GCODE-tiedostot ovat pelkkää tekstiä, joten voit avata ne millä tahansa tekstieditorilla. yleisiä tekstieditoreja ovat **Muistio (Windows)**, **TextEdit (macOS)** tai **Gedit (Linuxissa)**; **klikkaa hiiren kakkospainikkeella** G-kooditiedostoa, valitse **Avaa** ja valitse tekstieditori.

