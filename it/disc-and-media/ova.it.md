{
  "date" : "2021-08-10",
  "keywords" :[ "file .ova", "formato file", "cos'è un file .ova", "file", "estensione file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri cos'è un formato di file .ova e le API che possono creare e aprire file ova.",
  "title" :"Formato file OVA - Apri file dell'appliance virtuale",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Che cos'è un file OVA?

Un file OVA (Open Virtual Appliance) è una directory OVF salvata come archivio utilizzando il formato di archiviazione .tar. È un file di pacchetto dell'appliance virtuale che contiene i file per la distribuzione del software eseguito su una macchina virtuale. Un pacchetto OVA contiene un file descrittore [.ovf](/it/disc-and-media/ovf/), file di certificato, un file [.mf](/it/programming/mf/) opzionale insieme ad altri file correlati. I file OVA hanno il tipo di supporto come application/ovf.

## Formato file OVA

Come accennato, un file OVA è un file di archivio che viene creato utilizzando la directory OVF in formato file TAR. Il file stesso viene salvato come file binario. La maggior parte delle piattaforme di virtualizzazione, come VMware, Microsoft, Oracle e Citrix, possono installare dispositivi virtuali da un file OVF che è un file descrittore con i dettagli dell'immagine da caricare nella macchina virtuale.

## Vantaggi di un file OVA

* I file OVA sono compressi, consentendo download più veloci.
* Il client vSphere convalida un file OVA prima di importarlo e garantisce che sia compatibile con il server di destinazione previsto. Se l'appliance non è compatibile con l'host selezionato, non può essere importata e viene visualizzato un messaggio di errore.
* OVA può incapsulare applicazioni multilivello e più di una macchina virtuale.

## Riferimenti

* [Formati e modelli di file OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Specifiche del formato file OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualiization-format-specification-dsp0243_1-1-0.pdf)

