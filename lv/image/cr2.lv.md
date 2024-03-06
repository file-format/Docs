{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR2 faila formāts — Canon Raw 2 attēla fails",
  "description":"Uzziniet par CR2 faila formātu un API, kas var izveidot un atvērt CR2 failus.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2-lv",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Kas ir CR2 fails?

CR2 (Camera RAW 2) fails ir RAW attēla fails, kas izveidots ar Canon digitālajām kamerām. Tas saglabā sākotnējos neapstrādātos bezzudumu attēla datus, kas uzņemti ar kameru. CR2 faila formātu ir izstrādājis Canon savām digitālajām kamerām, un tas var ierakstīt augstas kvalitātes attēlus līdz pat 14 bitiem RGB. Tādējādi tiek iegūti augstas kvalitātes attēli ar pietiekami daudz vietas pēcapstrādei. CR2 attēla formātu Canon ir izmantojis savos 350D, 20D un 1D kameru modeļos. CR2 faili ir RAW faili un satur papildu metadatu informāciju, piemēram, informāciju par kameru, objektīva informāciju, dublēšanas informāciju, baltā balansu un citus iestatījumus.

## CR2 faila formāts

CR2 faili tiek saglabāti kameras atmiņas kartē kā bināri faili Canon patentētā faila formātā. CR2 faila formāts aizstāja sākotnēji izmantoto CRW faila formātu un vēlāk tika aizstāts ar Canon RAW 3 faila formātu. CR2 faila formāts ir balstīts uz [TIFF](/image/tiff/) specifikācijām, kurām ir 4 attēlu failu direktoriji (IFD).

|Nobīde |Saturs |Komentārs|
---|---|---|
|0x0000 |Galvene |satur baitu secību, versiju un nobīdi pret RAW attēlu|
|aprēķināts |IFD#0 |šajā daļā ir Exif sadaļa, kurā ir sadaļa Makernotes.
Informācija par attēlu#0|
|aprēķināts |attēls#0 |maza attēla versija (viena ceturtā daļa no oriģināla izmēra), saspiesta Jpeg|
|aprēķināts |IFD#1 |Informācija par attēlu#1.|
|aprēķināts |attēls#1 |maza attēla versija, saspiesta Jpeg|
|aprēķināts |IFD#2 |Informācija par attēlu#2.|
|aprēķināts |attēls#2 |maza attēla versija, nesaspiesta|
|galvenē| IFD#3| Informācija par 3. attēlu, pilna izmēra RAW attēlu|
|aprēķināts |attēls#3 |RAW attēla dati, bez zudumiem saspiesti Jpeg formātā (nevis RGB dati!)|

## CR2 faila formāta priekšrocības

Attēlu saglabāšana RAW formātā ļauj veikt daudz fotogrāfijas pēcapstrādes, piemēram, pielāgot baltā balansu. Tas ir daudz grūtāk un ar lielu kvalitātes zudumu, izmantojot citus attēlu failu formātus, piemēram, [JPEG](/image/jpeg/).

## Vai CR2 ir labāks par JPEG?

CR2 faili ir neapstrādāti faili, nezaudējot datus un tādējādi nezaudējot kvalitāti. No otras puses, JPEG ir attēla faila formāts ar zudumiem, jo tiek zaudēti daži dati, lai samazinātu failu. Tādējādi CR2 faili ir augstas kvalitātes un piemērotāki retušēšanai un uzlabojumiem.

## Atsauces

 * [CR2 faila formāts] (http://lclevy.free.fr/cr2/)

