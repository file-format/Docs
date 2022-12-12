{
  "date" : "2021-08-10",
  "keywords" :[ "fișier .ovf", "format fișier", "ce este un fișier .ovf", "fișier", "extensie fișier"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre ce este un format de fișier .ovf și API-urile care pot crea și deschide fișiere OVF.",
  "title" :"Format fișier OVF - Deschideți fișierul de virtualizare",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Ce este un fișier OVF?

Un fișier OVF este un fișier text care conține informații despre ambalarea și distribuția unui software care rulează pe o mașină virtuală. Este formatat conform [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) care descrie toate cerințele (cum ar fi securitatea, portabilitatea, eficiența și extinderea) pentru rularea aplicațiilor pe mașinile virtuale. Organizația Internațională pentru Standardizare (ISO) a adoptat OVF ca standard ISO 17203.

## Scurt istoric al formatului de fișier OVF

Formatul de fișier OVF a fost introdus de DMTF (Distributed Management Task Force) care creează standarde deschise de gestionare. Este independent de orice arhitectură specială de hipervizor sau set de instrucțiuni. Pachetul OVF conține unul sau mai multe sisteme virtuale, fiecare dintre acestea putând fi implementat pe o mașină virtuală.

## Format de fișier OVF - Mai multe informații

Un pachet OVF constă din mai multe fișiere plasate într-un singur director. Printre acestea, conține exact un fișier descriptor OVF (cu extensia .ovf) care este stocat în format de fișier [XML](/ro/web/xml/). Descrie informațiile despre mașina virtuală ambalate și informațiile despre metadate despre pachetul OVF, cum ar fi:

* Nume
* cerințe hardware
* referințe la celelalte fișiere din pachetul OVF și
* descrieri care pot fi citite de om

Alte fișiere care pot fi găsite într-un pachet OVF includ una sau mai multe imagini de disc și, opțional, fișiere de certificat și alte fișiere auxiliare.

## Referințe

* [Format de virtualizare deschis - DMTF](https://www.dmtf.org/standards/ovf)
* [Specificații de format de fișier OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

