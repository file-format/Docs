{
  "date" : "2021-08-11",
  "keywords" :[ "fișier vdi", "format fișier vdi", "ce este un fișier vdi", "fișier", "exemplu vdi", "extensie fișier vdi", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier VDI și despre API-urile care pot crea și deschide fișiere VDI.",
  "title" :"VDI - Fișier imagine disc virtual VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Ce este un fișier VDI?
Un fișier cu extensia .vdi este o imagine de disc virtual; specific programului de virtualizare desktop open source Oracle numit VirtualBox. Fișierele VDI sunt folosite pentru a porni mașina virtuală VirtualBox. VM-urile permit utilizatorilor să ruleze sisteme de operare sau programe suplimentare pe un singur computer. Prin urmare, avantajul fișierelor VDI este că utilizatorii pot salva aceste fișiere de imagine de disc pe hard disk și le pot rula folosind emulatori ori de câte ori au nevoie.

## Format de fișier VDI
Virtual Disk Image (VDI) este formatul principal de fișier de disc pentru o mașină virtuală Oracle open-source dezvoltată activ, cunoscut sub numele de VirtualBox, care este un produs de virtualizare de clasă enterprise. Formatul de fișier VDI este conceput pentru a crea o imagine de disc portabilă care poate fi rulată cu ușurință folosind alte programe de virtualizare. Acceptă atât stocarea alocată dinamic, cât și stocarea de dimensiuni fixe. Vă permite să extindeți un fișier imagine după ce a fost creat, chiar dacă acesta conține deja date.

### Virtualizare disc
Sistemul emulează hard disk-uri în format de imagine disc VDI. O VM VirtualBox poate folosi discuri anterioare create în Microsoft Virtual PC sau VMware, precum și propriul format nativ. VirtualBox este, de asemenea, capabil să se conecteze la ținte iSCSI și să partiționeze brut pe gazdă, folosind fie ca hard disk-uri virtuale. VirtualBox emulează IDE (controlere PIIX4 și ICH6), SATA (controler ICH8M), controlere SAS la care se pot atașa hard disk-uri și SCSI.

Suportul este disponibil pentru Open Virtualization Format (OVF) începând cu versiunea 2.2.0 a VirtualBox. Atât dispozitivele fizice conectate la gazdă, cât și imaginile ISO pot fi montate ca unități CD sau DVD.
În mod implicit, VirtualBox acceptă grafică printr-o placă grafică virtuală personalizată compatibilă VESA.

### Suport de virtualizare pentru Ethernet
VirtualBox virtualizează următoarele plăci de interfață de rețea pentru un adaptor de rețea Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Desktop Intel Pro/1000 MT (82540EM)
- Server Intel Pro/1000 MT (82545EM)
- Server Intel Pro/1000 T (82543GC)
- Adaptor de rețea paravirtualizat (virtio-net)

Plăcile de rețea emulate permit sistemelor de operare invitate să ruleze fără a fi nevoie să căutați și să instalați drivere pentru hardware-ul de rețea, deoarece acestea sunt disponibile ca parte a sistemului de operare invitat. Un adaptor de rețea paravirtualizat special îmbunătățește performanța rețelei reducând nevoia de a se potrivi cu o interfață hardware specifică. Prin urmare, necesită asistență specială pentru șofer la oaspete.


## Referințe

* [VirtualBox - de la Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


