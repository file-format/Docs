{
  "date" : "2021-08-10",
  "keywords" :[ "fișier .ova", "format fișier", "ce este un fișier .ova", "fișier", "extensie fișier"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre ce este un format de fișier .ova și API-urile care pot crea și deschide fișiere ova.",
  "title" :"Format fișier OVA - Deschideți fișierul aparatului virtual",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Ce este un fișier OVA?

Un fișier OVA (Open Virtual Appliance) este un director OVF salvat ca arhivă folosind formatul de arhivare .tar. Este un fișier de pachet de dispozitiv virtual care conține fișiere pentru distribuirea de software care rulează pe o mașină virtuală. Un pachet OVA conține un fișier descriptor [.ovf](/ro/disc-and-media/ovf/), fișiere de certificat, un fișier opțional [.mf](/ro/programming/mf/) împreună cu alte fișiere conexe. Fișierele OVA au tipul media ca aplicație/ovf.

## Format de fișier OVA

După cum sa menționat, un fișier OVA este un fișier de arhivă care este creat folosind directorul OVF în format de fișier TAR. Fișierul în sine este salvat ca fișier binar. Majoritatea platformelor de virtualizare, cum ar fi VMware, Microsoft, Oracle și Citrix, pot instala dispozitive virtuale dintr-un fișier OVF care este un fișier descriptor care conține detaliile imaginii care urmează să fie încărcate în mașina virtuală.

## Avantajele unui fișier OVA

* Fișierele OVA sunt comprimate, permițând descărcări mai rapide.
* Clientul vSphere validează un fișier OVA înainte de a-l importa și se asigură că este compatibil cu serverul de destinație dorit. Dacă aparatul este incompatibil cu gazda selectată, acesta nu poate fi importat și apare un mesaj de eroare.
* OVA poate încapsula aplicații cu mai multe niveluri și mai mult de o mașină virtuală.

## Referințe

* [Formate și șabloane de fișiere OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Specificații de format de fișier OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

