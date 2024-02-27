{
  "date": "2019-10-11",
  "keywords": [
"bmp fil",
"bmp filformat",
"hvad er en bmp-fil",
"fil",
"bmp eksempel",
"bmp filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP - Billedfilformat",
  "description": "Lær om BMP-filformat og API'er, der kan oprette og åbne BMP-filer.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-dap"
}
},
  "lastmod": "2019-09-10"
}

# Hvad er en BMP-fil? #

Filer med filtypenavnet .BMP repræsenterer bitmapbilledfiler, der bruges til at gemme digitale bitmapbilleder. Disse billeder er uafhængige af grafikadapter og kaldes også enhedsuafhængigt bitmap-filformat (DIB). Denne uafhængighed tjener det formål at åbne filen på flere platforme såsom Microsoft Windows og Mac. BMP-filformatet kan gemme data som todimensionelle digitale billeder i både monokrome såvel som farveformater med forskellige farvedybder.

## BMP-filformatspecifikationer ##

Enhedsuafhængige bitmaps fungerer som en hjælp til udveksling af bitmaps mellem enheder og applikationer. På grund af den kontinuerlige udvikling af dette filformat kan oplysningerne i overskrifterne være forskellige i henhold til versionen af Bitmap. En enkelt bitmap-fil består af faste såvel som variabel størrelse strukturer i en bestemt rækkefølge.

Strukturer i en bitmap-fil er arrangeret i følgende rækkefølge:


|Struktur|Valgfri|Størrelse|Formål
---|---|---|---|
|File Header|No|14|At gemme generel information om bitmap-billedfilen
|DIB Header|No|Fixed-Size|At gemme detaljerede oplysninger om bitmapbilledet og definere pixelformatet
|Ekstra bitmasker|Ja|12 eller 16 bytes|For at definere pixelformatet
|Farvepalet|Semi-valgfri|Variabel størrelse|For at definere farver, der bruges af bitmap-billeddata
|Gap1|Ja|Variabel størrelse|Strukturjustering
|Pixel Array|No|Variabel-størrelse|Pixelformat er defineret af DIB-headeren eller Ekstra bitmaskerne.
|Gap2|Ja|Variabel størrelse|Strukturjustering
|ICC Farveprofil|Ja|Variabel størrelse|For at definere farveprofilen til farvestyring

Når et bitmapbillede indlæses i hukommelsen, bliver det en DIB-struktur, der bruges af Windows via dets GDI API. Filoverskriften er ikke en del af denne datastruktur. Farven kan også bestå af 16-bit indgange, der udgør indekser til den aktuelt refererede palette i stedet for eksplicitte RGB-farvedefinitioner. Lad os se på nogle af disse i detaljer, især overskrifterne.

### Bitmap-filoverskrift ###

En Bitmap File Header ligner andre filheadere, der bruges til at identificere filen. Da der er forskellige varianter af BMP-filformatet, er de første 2 bytes af BMP-filformatet tegn B og derefter tegn M i ASCII-kodning. Alle heltalsværdier gemmes i lille endian-format.

|Offset hex|Offset dec|Størrelse|Formål
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2 struct bitmap array * **CI** – OS/2 struct farveikon * **CP** – OS/2 const farvemarkør * **IC** – OS/2 struct ikon * **PT** – OS/2 pointer
|02|2|4 bytes|Størrelsen af BMP-filen i bytes
|06|6|2 bytes|Reserveret; faktisk værdi afhænger af den applikation, der skaber billedet
|08|8|2 bytes|Reserveret; faktisk værdi afhænger af den applikation, der skaber billedet
|0A|10|4 bytes|Forskydningen, dvs. startadressen, for den byte, hvor bitmap-billeddataene (pixelarray) kan findes.

#### DIB header (bitmap information header) ####

De detaljerede oplysninger om billedet er repræsenteret af denne overskrift. Baseret på disse oplysninger, vil applikationen blive bestemt, der vil blive brugt til at vise billedet på skærmen. Alle sådanne overskrifter indeholder et DWORD (32-bit) felt, der angiver deres størrelse, så en applikation nemt kan bestemme den overskrift, der bruges i billedet. Dette skyldes i bund og grund, at DIB-formatet har gennemgået flere udvidelser. Følgende er DIB-headeren med anførte felter.

#### Farvepalet ####

En BMP-farvepalet er en række strukturer, der angiver RGB-intensitetsværdierne for hver farve i en skærmenheds farvepalet. Hver pixel i bitmapdataene gemmer en enkelt værdi, der bruges som et indeks i farvepaletten. Farveinformationen, der er gemt i elementet ved det indeks, angiver farven på den pixel. Tilgængeligheden af farver i en bitmap-fil varierer som følger:

* En, 4 og 8-bit - forventes altid at indeholde en farvepalet

* Seksten, 24 og 32-bit - indeholder aldrig farvepaletter

* Seksten og 32-bit BMP-filer - indeholder bitfeltmaskeværdier i stedet for farvepaletten


#### Pixel Storage ####

Bitmappixels gemmes som bits pakket i rækker, hvor størrelsen af hver række rundes op til et multiplum af 4 bytes (en 32-bit DWORD) ved udfyldning. Den samlede mængde bytes, der kræves for at gemme pixels i et billede, kan ikke beregnes direkte ved blot at tælle bits. Da der er polstring involveret, er effekten af at runde størrelsen af hver række op til et multiplum af 4 bytes påkrævet. Udfyldningsbytes (ikke nødvendigvis 0) skal tilføjes til slutningen af rækkerne for at bringe længden af rækkerne op til et multiplum af fire bytes. Når pixel-arrayet er indlæst i hukommelsen, skal hver række begynde ved en hukommelsesadresse, der er et multiplum af 4.

Billedet er faktisk beskrevet af 32-bit DWORDs repræsentation af pixel arrayet. Normalt lagres pixels bottom-up, startende i nederste venstre hjørne, fra venstre mod højre og derefter række for række fra bunden til toppen af billedet. Pixelformater og deres implikationer er som angivet nedenfor:

* Formatet 1-bit pr. pixel (1bpp) understøtter 2 forskellige farver (f.eks. sort og hvid).

* 2-bit pr. pixel (2bpp)-formatet understøtter 4 forskellige farver og lagrer 4 pixel pr. 1 byte, hvor den længst til venstre er i de to mest signifikante bits. Hver pixelværdi er et 2-bit indeks i en tabel med op til 4 farver.

* 4-bit pr. pixel (4bpp)-formatet understøtter 16 forskellige farver og gemmer 2 pixel pr. 1 byte, hvor pixel længst til venstre er i den mere signifikante nibble. Hver pixelværdi er et 4-bit indeks i en tabel med op til 16 farver.

* 8-bit pr. pixel (8bpp) formatet understøtter 256 forskellige farver og gemmer 1 pixel pr. 1 byte. Hver byte er et indeks til en tabel med op til 256 farver.

* 16-bit pr. pixel (16bpp)-formatet understøtter 65536 forskellige farver og gemmer 1 pixel pr. 2-byte WORD. Hvert ORD kan definere alfa, røde, grønne og blå prøver af pixlen.

* 24-bit pixelformatet (24bpp) understøtter 16.777.216 forskellige farver og gemmer 1 pixelværdi pr. 3 bytes. Hver pixelværdi definerer de røde, grønne og blå prøver af pixlen (8.8.8.0.0 i RGBAX-notation). Specifikt i rækkefølgen: blå, grøn og rød (8 bits pr. prøve).

* 32-bit pr. pixel (32bpp)-formatet understøtter 4.294.967.296 forskellige farver og gemmer 1 pixel pr. 4-byte DWORD. Hvert DWORD kan definere alfa, røde, grønne og blå prøver af pixlen.


## Referencer ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP-filformat](https://en.wikipedia.org/wiki/BMP_file_format)


