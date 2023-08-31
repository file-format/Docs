{
  "date" : "2021-08-09",
  "keywords" :[ "fișier CSO", "format fișier CSO", "ce este un fișier CSO", "fișier", "exemplu CSO", "extensie fișier CSO", "extensie", "format", "iso", "compresie DAX "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier CSO și despre API-urile care pot crea și deschide fișiere CSO.",
  "title" :"CSO – Imagine de disc ISO comprimată",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Ce este un fișier CSO?

Un fișier cu extensia .cso este un fișier imagine ISO comprimat. CSO este o alternativă la metoda de compresie DAX; cunoscut și ca CISO; a fost prima metodă de comprimare a fișierelor [ISO](/ro/compression/iso/) și este de obicei o metodă preferată pentru arhivarea lucrurilor PlayStation Portable. Acest format folosește compresia Deflate, care poate include până la nouă straturi de compresie. Pentru a crea imaginile sunt folosite programe precum Prometheus și YACC.

## Format de fișier CSO

Formatul de fișier CSO a fost prima metodă de compresie pentru ISO pentru a economisi mai mult spațiu de memorie. Îmbunătățirile au fost făcute din când în când pentru o compresie mai bună. CSO utilizează compresia Deflate având nouă nivele de presetări, de obicei, fiecare nivel poate gestiona 2 blocuri KiB individual. În timp ce cele mai înalte niveluri de compresie pot încetini și prelungi timpii de încărcare în software, care depind în mare măsură de fluxul de disc, de asemenea, nivelurile inferioare pot efectua o compresie substanțială.

### Structura fișierului CSO

Formatul de fișier CSO conține un antet de 24 de octeți, blocuri de date și un tabel de index. Little-endian se presupune pentru câmpuri mai mari decât un octet. Caracteristicile arhitecturii PlayStation Portable sunt prezentate mai jos.

#### Antet

| Offset (octeți) | Nume | Dimensiune (octeți) | Scop |
----------|----------|--------------|---------|
| 0x0 | Magie | 4 | Întotdeauna CISO sau 0x4F534943 când este citit ca un întreg pe 32 de biți. Acest câmp este folosit pentru a identifica un fișier CSO. Rețineți că acest câmp poate fi diferit pentru celelalte derivate ale CSO, de exemplu, ZSO a folosit codul magic ZISO. |
| 0x4 | Dimensiunea antetului | 4 | Pentru formatul original de fișier CSO „v1”, acest câmp este ignorat și, prin urmare, nu este necesar să fie exact. Cu toate acestea, formatul „v2” și ZSO necesită ca acest câmp să fie întotdeauna 0x18 (24 de octeți). |
| 0x8 | Dimensiune necomprimată | 8 | Dimensiunea ISO original necomprimat în octeți. |
| 0x10 | Dimensiunea blocului | 4 | Dimensiunea fiecărui bloc de date în octeți înainte de comprimare. De obicei, 2048 de octeți, la fel ca dimensiunea fiecărui sector ISO 9660. |
| 0x14 | Versiune | 1 | Versiunea formatului de fișier utilizat. Pentru formatul „v1”, valoarea poate fi fie 0, fie 1. Pentru formatul „v2”, acesta trebuie să fie 2. În plus, formatul ZSO necesită ca acesta să fie 1. |
| 0x15 | Alinierea indexului | 1 | Alinierea fiecărei intrări de index, specificată în biți. |
| 0x16 | Rezervat | 2 | Acest câmp este neutilizat. În formatul „v1”, acest câmp este ignorat și poate conține valori arbitrare. În formatul „v2”, acest câmp trebuie să fie zero. |

#### Tabel index

Tabelul de index conține mai multe intrări de 4 octeți, care indică poziția fiecărui bloc de date și o ultimă intrare suplimentară care indică sfârșitul fișierului.
Conținutul fiecărei intrări este următorul:
| Bit | Lungime | Masca | Nume | Scop |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Poziția | Acest câmp, atunci când este deplasat la stânga de alinierea indexului dată în antet, indică poziția în care începe blocul de date. |
| 31 | 1 | 0x80000000 | Tip de compresie | Formatul ZSO are o semantică similară, doar că 0 reprezintă LZ4 în loc de Deflate. În formatul „v2”. Blocul este implicit considerat a fi necomprimat dacă dimensiunea blocului este egală sau mai mare decât dimensiunea blocului specificată în antetul fișierului. |

#### Blocuri de date

Blocurile de date cuprind date necomprimate sau comprimate. Mărimea unui bloc este calculată obținându-i poziția și apoi scăzând-o din poziția blocului următor. Dacă alinierea indexului este mai mare decât zero, este probabil ca dimensiunea blocului să fie mai mare decât datele pe care le deține.


## Referințe

* N/A

