{
  "date": "2019-10-11",
  "keywords": [
"j2c failu",
"j2c faila formāts",
"kas ir j2c fails",
"failu",
"j2c piemērs",
"j2c faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "Uzziniet par J2C faila formātu un API, kas var izveidot un atvērt J2C failus.",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-lvc"
}
},
  "lastmod": "2021-02-14"
}

## Kas ir J2C fails?

Fails ar paplašinājumu .j2c ir JPEG faila formāta variants, un tas ir saspiests, izmantojot viļņu saspiešanu. Tam ir gandrīz identiska marķieru un segmentu sistēma JPEG 2000 faila formātam. J2C faila formāts ir definēts JPEG 2000 statīva 1. daļā, kas atbalsta gan zudumu, gan bezzudumu saspiešanu. JPEG 2000 kodu straume tika izstrādāta iegulšanai [JP2](/image/jp2/) vai citā faila formātā, lai gan tā var parādīties failā pati par sevi. J2C failu var atvērt, izmantojot programmas Adobe Photoshop 2020, Adobe Illustrator 2020 un Corel Paintshop Pro.

## J2C faila formāts

J2C faila formāts ir tāds pats kā JPEG 2000, kas bieži tiek saglabāts kā .jp2 un .jpc. Tas liek J2C failiem izmantot to pašu pieeju metadatu kodēšanai XML formātā, kur standarts 12234-1 tiek izmantots kā atsauce starp Exif tagiem un XML komponentiem. To vēl vairāk uzlabo JPEG 2000 2. daļas paplašinājums, kas apvieno animācijas mehānismu un koda straumes konfigurācijas vienā attēlā. Šādi paplašināti faila formāta faili tiek saglabāti kā [.jpx](/image/jpx/).

### JPEG2000 faila izkārtojums

JPEG2000 atbalsta dažādas lietojumprogrammas, kuru pamatā ir atbilstība paplašināmiem failu formātiem. Lai gan vienkāršākais veids var ietvert vienu attēlu, sarežģītākos veidos var būt attēlu sērija, kas ir sakrauta viens virs otra vai ir secīgi secīgi.

#### JP2 kaste
Tas ir JP2 faila formāta augstākā līmeņa veidošanas bloks, un galvenē ir ietverti tipa un garuma lauki, kā arī datu sadaļa. Visievērojamākais kastes veids ir blakus esošā koda straumes kaste. Šī lodziņa datu sadaļā tiek saglabāta JPEG2000 kodu straume.

#### JPEG2000 CodeStream

JPEG2000 CodeStream ir baitu secība, kas nepieciešama JPEG2000 saspiestā attēla atkodēšanai. Ja failam nav nekā cita, izņemot šo koda straumi, to sauc par neapstrādātu koda straumes failu. Parasti JPEG koda straume ir JPEG2000 kompresijas algoritma pielietojums attēlam, lai gan tas nav vienīgais veids.

#### Flīžu daļas ####

JPEG2000 kodēts attēls ir datu vienību kopums, ko sauc par paketēm. Šīs paketes tiek uzturētas kodu plūsmā pakešu grupās, ko sauc par elementu daļām. Pirms attēla kodēšanas kodētājs attēlu sadala taisnstūrveida bloku režģī, ko sauc par flīzēm, kur katra flīze tiek kodēta atsevišķi neatkarīgi no citiem elementiem.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 faila formāts" >}}

## J2C kompresija
JPEG 2000 izmanto viļņu saspiešanas tehnoloģiju, padarot to ātru, pamatojoties uz to, ka tiek parādīts salīdzinoši maz pikseļu jebkurā skatvietā vai logā, ko skatītājs parāda. To var uzsvērt ar to, ka ļoti liela izmēra attēliem (gigabaitos) ekrānā parādīsies tikai daži megabaiti pikseļu. Tas palīdz ātri iegūt un renderēt tikai to attēla datu daļu, kas nepieciešama displeja pikseļu aizpildīšanai. Tam nepieciešama arī ātrgaitas dekompresijas tehnoloģija, lai paātrinātu attēlu iegūšanas mehānismu, lai izveidotu vajadzīgos attēlus lidojumā.

J2C izmanto ātrās dekompresijas priekšrocības un ienes tikai nepieciešamo informāciju pikseļu datiem, lai ekrānos ātri parādītu daļu no redzamajiem attēliem. J2C galvenokārt ir paredzēts datu apskatei, nevis to rediģēšanai.

## J2C identifikācija
JPEG 2000 failiem ir paraksta baiti FF 4F FF 51.

### Mīmikas veidi
Reģistrētie MIME tipi JPEG 2000 failiem ietver:
  * attēls/j2c
  * attēls/jpx
  * attēls/jpm
  * video/mj2

## Uzlabojumi salīdzinājumā ar JPEG standartu
Uzlabojumi salīdzinājumā ar JPEG standartu ietver:
  * Izcila kompresijas veiktspēja
  * Vairāku izšķirtspējas attēlojums
  * Progresīva pārraide pa pikseļiem un izšķirtspējas precizitāte
  * Bezzudumu vai zudumu saspiešanas izvēle
  * Kļūdu noturība, elastīgs faila formāts
  * Augsta dinamiskā diapazona atbalsts
  * Sānu kanāla telpiskā informācija

## Atsauces Nr.
  * [Taubmans, Deivids; Marselins, Maikls (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

