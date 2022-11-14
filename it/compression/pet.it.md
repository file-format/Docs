{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PET - File pacchetto di installazione Puppy Linux",
  "description":"Scopri il formato di file PET e le API che possono creare e aprire file PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Che cos'è un file PET di Linux?

Un file PET è un file del pacchetto di installazione dell'applicazione creato e utilizzato con la variante PuppyLinux del sistema operativo Linux. Viene creato come file compresso [TGZ](/it/compression/tgz/) che riduce la dimensione del file dell'archivio compresso. L'integrità del formato del file PET è garantita dal checksum md5sum che viene aggiunto alla fine del file per la verifica all'estremità remota. I file PET possono essere estratti utilizzando l'estrattore di file TGZ standard e WinRAR. I file PET hanno sostituito i vecchi file di installazione del pacchetto [PUP](/it/compression/pup/).

## Formato file PET

I file PET vengono salvati su disco come archivi compressi in formato binario. Tuttavia, i dettagli del formato file interno del formato file PET non sono noti. Simile ai file di installazione dei pacchetti [.exe](/it/executable/exe/) e [.msi](/it/executable/msi/), i file PET avviano un'installazione quando vengono eseguiti.

## Riferimenti

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Indice dei pacchetti PET di PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

