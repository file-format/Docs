{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Dispositivo eBook Rocket di Nuvo Media", "file", "estensione", "formato", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file RB per il dispositivo eBook Rocket di Nuvo Media e le API che possono creare e aprire file RB.",
  "title" :"RB - File eBook Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Che cos'è un file RB?

Il file con estensione .rb contiene il contenuto dell'eBook Rocket. L'eBook Rocket è in realtà un dispositivo realizzato da Nuvo Media; hanno rilasciato questo dispositivo nel 1998. Sebbene Rocket eBook sia in grado di visualizzare immagini, ma solo in bianco e nero. Ha uno schermo di 106 dpi o 480 x 320 pixel su un touch screen da 4,5 x 3 pollici. L'eBook Rocket si collega a un computer tramite una porta seriale per scaricare eBook in formato file RB. I file RB sono in grado di utilizzare DRM ma questa tecnologia non viene utilizzata negli eBook moderni. Il file RB contiene convenzionalmente un file HTML con le immagini e un file pseudo-OPF con tutti i metadati (.info).

## Specifiche tecniche del formato file RB ##

Un numero magico (in esadecimale) appare nei primi 4 byte del file: B0 0C B0 0C.

Sembra che i due byte successivi siano un numero di versione, come "02 00", che sta per major version 2 e minor version 0.

I successivi quattro byte contengono il testo "NUVO", seguito da 4 byte di 00h.

I successivi 4 byte sono la data di creazione del libro, codificata come int16. Questo ci pone all'offset 0Eh. La vecchia versione di ORocketLibrary codificava il valore completo dell'anno (cioè, il 1999 era "CF 07", il 2000 era "D0 07"). Nella versione recente, tm_year è memorizzato testualmente, ovvero 100 per l'anno 2000 ("64 00"). Dopo l'anno viene un int8 che rappresenta il numero del mese relativo a 1 e un int8 che rappresenta il giorno del mese.

I prossimi 6 byte sono 00h. Per l'impostazione dell'ora, questi possono essere riservati.

L'offset assoluto del "Sommario" è contenuto in un int32 all'offset 18h.

Dopo questo è un int32 contenente la lunghezza del file .rb. Viene utilizzato per determinare se i file sono completi o meno.

L'intero blocco di byte (da 20 ore a 128 ore) sembra essere necessario solo per un titolo crittografato. Nei titoli non crittografati, sono sempre zero.

Nella maggior parte dei casi, segue il sommario (all'offset 128). Inizia con un conteggio int32 del numero di voci di "pagina" (sezioni di file .rb) nel ToC. Ciascuna voce è composta da un nome (con riempimento a 32 byte), seguito da 3 int32: la lunghezza del segmento di dati, la posizione nel file .rb e un flag per questa voce. Ad oggi, i valori noti sono: 1 (crittografato), 2 (pagina informativa) e 8 (sgonfiato). I nomi sono tutti adattati, se necessario, per garantire che siano tutti unici.

## Riferimenti

* [E-Reader - Da MobileRead](https://en.wikipedia.org/wiki/E-reader)

