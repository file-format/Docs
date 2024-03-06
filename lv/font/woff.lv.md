{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - Web Open File Format",
  "description": "WOFF fails ir atvērts fonta formāts, kas izveidots Web Open Font Format formātā.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-lvf"
}
},
  "lastmod": "2020-09-30"
}

## Kas ir WOFF fails?

Fails ar paplašinājumu .woff ir tīmekļa fonta fails, kura pamatā ir Web Open Font Format (WOFF). Tam ir formātam specifisks saspiests konteiners, kura pamatā ir TrueType (.TTF) vai OpenType (.OTT) fontu tipi. WOFF tika ieviests ar mērķi atšķirt tīmekļa fontus no fontu failiem, ko izmanto darbvirsmas lietojumprogrammās. Turklāt formāts ir paredzēts, lai samazinātu fontu pārsūtīšanas latentumu no servera uz klienta datoru tīklā. Ir pieejami vairāki rīki, kas var konvertēt WOFF failus uz TTF un citiem fontu failu formātiem.

## WOFF faila formāts

WOFF fonta formāts saspiež uz tabulu balstītu sfnt struktūru fontu datu tabulas, ko izmanto dažādos fontu tipos, piemēram, TrueType, OpenType un Open Font Format. Tas ir kā konteiners šiem fontu veidiem, un tajā ir arī vieta, kur iekļaut fonta metadatus un privātas lietošanas datus, kas jāiekļauj konteinerā. Pārveidotāji izmanto sfnt failus WOFF formāta failā, un lietotāju aģenti atjauno kodēto failu lietošanai ar tīmekļa dokumentu. Jāatzīmē, ka atjaunotie fontu dati no visiem aspektiem precīzi atbilst ievades fonta formātam.

WOFF failu utilītas bieži satur papildu līdzekļus, piemēram, glifu apakškopu, validāciju vai fontu funkciju papildinājumus, taču tas nav nepieciešams. Gan izveidotājam, gan izmantošanas aģentiem ir jānodrošina pamatā esošo fontu datu derīguma saglabāšana.

### WOFF faila struktūra

WOFF faila struktūra ir līdzīga sfnt fontu struktūrai. Tas ir balstīts uz tabulu direktoriju, kurā ir katra fonta datu tabulas garums un nobīdes. Pēc šīs sākotnējās informācijas tiek ievērotas visas tabulas. Failā ir fontu datu bāze, kas ir tāda pati kā oriģinālajos fontos. Tabulu secība arī ir vienāda, taču katra var būt saspiesta. Tomēr WOFF tabulas direktorijs aizstāj sākotnējo tabulas direktoriju.

WOFF fails sastāv no šādiem elementiem:

 * WOFFHeader — faila galvene ar pamata fonta veidu un versiju, kā arī metadatu un privāto datu bloku nobīdēm.
 * TableDirectory — fontu tabulu direktorijs, kas norāda katras tabulas sākotnējo izmēru, saspiesto izmēru un atrašanās vietu WOFF failā.
 * FontTables — fontu datu tabulas no ievades sfnt fonta, saspiestas, lai samazinātu joslas platuma prasības.
 * ExtendedMetadata — neobligāts paplašināto metadatu bloks, kas attēlots XML formātā un saspiests glabāšanai WOFF failā.
 * PrivateData — izvēles privāto datu bloks, ko izmantot fontu izstrādātājam, lietuvei vai pārdevējam.

### WOFF galvene
WOFF galvene sastāv no identificējoša paraksta, kas norāda failā iekļauto datu veidu. WOFF galvene kopā ar tās laukiem ir šāda.

|Tips|Lauka nosaukums|Apraksts|
---|---|---|
|UInt32|paraksts |0x774F4646 'wOFF' |
|UInt32| flavor |Ievades fonta sfnt versija.|
|UInt32| garums |WOFF faila kopējais lielums.|
|UInt16| numTables |Ierakstu skaits fontu tabulu direktorijā.|
|UInt16| rezervēts |Rezervēts; iestatīts uz nulli.|
|UInt32| totalSfntSize |Kopējais lielums, kas nepieciešams nesaspiestiem fontu datiem, tostarp sfnt galvenei, direktorijam un fontu tabulām (ieskaitot pildījumu).|
|UInt16| majorVersion |WOFF faila galvenā versija.|
|UInt16| minorVersion |WOFF faila neliela versija.|
|UInt32| metaOffset |Nobīde uz metadatu bloku, no WOFF faila sākuma.|
|UInt32| metaLength |Saspiestā metadatu bloka garums.|
|UInt32| metaOrigLength |Nesaspiests metadatu bloka izmērs.|
|UInt32| privOffset |Nobīde uz privāto datu bloku, no WOFF faila sākuma.|
|UInt32| privLength |Privātā datu bloka garums.|

## Atsauces

 * [w3 WOFF faila formāts](https://www.w3.org/TR/WOFF/)

