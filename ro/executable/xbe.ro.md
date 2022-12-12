{
  "date" : "2021-08-31",
  "keywords" :[ "fișier xbe", "format fișier xbe", "ce este un fișier xbe", "fișier", "exemplu xbe", "extensie fișier xbe", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier XBE și despre API-urile care pot crea și deschide fișiere XBE.",
  "title" :"XBE – fișierul pachetului de aplicații iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Ce este un fișier XBE?
Un fișier cu extensia .xbe este o aplicație executabilă de pe un disc de jocuri video Xbox. Fișierele XBE sunt fișierele principale care sunt executate în sistemul Xbox și nu ar trebui să fie deschise de obicei pe un computer, dar pot fi deschise pe un computer folosind un program de emulare Xbox. Aceste fișiere sunt de obicei create de dezvoltatorii de jocuri și apoi semnate de Microsoft. Structura fișierelor este similară cu fișierele Windows PE, dar unele modificări importante în conformitate cu setările XBox sunt aplicate pentru a-l face rulabil pe XBox.

## Format de fișier XBE
Fișierul XBE este compus dintr-un antet de imagine, o colecție de anteturi de secțiune, un certificat, date de stocare locală a firului de execuție, o colecție de versiuni de bibliotecă, bitmap Microsoft și secțiunile care conțin codul și resursele.

### Antet imagine
Antetul imaginii cuprinde informațiile care explică unde se află celelalte componente ale executabilului în fișier și cum ar trebui să fie tratat și încărcat fișierul rulabil.

### Tabel TLS
Tabelul TLS constă din toate informațiile necesare XBE pentru a configura corect stocarea locală a firelor. Este practic unic pentru directorul TLS găsit în fișierele PE32 și poate fi copiat direct de acolo. Acest tabel poate fi omis, dacă fișierul XBE nu folosește nicio stocare locală de fir și câmpul respectiv din antetul imaginii este setat la zero.

| Offset | Dimensiune | Nume | Descriere |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Date brute Start | Adresă absolută (adică nu o RVA) de început a datelor variabilei TLS din imaginea programului. |
| 0x0004 | 0x0004 | Sfârșitul datelor brute | Adresă absolută (adică nu o RVA) a sfârșitului datelor variabilei TLS din imaginea programului. |
| 0x0008 | 0x0004 | Adresa indexului | Adresă absolută (adică nu o RVA) a variabilei Index TLS. |
| 0x000C | 0x0004 | Adresa apelurilor inverse | Adresă absolută (adică nu o RVA) a tabelului cu funcții de apel invers TLS terminat cu nul. |
| 0x0010 | 0x0004 | Dimensiunea umplerii zero | Numărul de octeți care urmează datelor brute care ar trebui setat la zero în memorie. |
| 0x0014 | 0x0004 | Caracteristici | Descrie alinierea. |

### Certificat

Un certificat a este obligatoriu pentru fiecare executabil Xbox care conține informații despre titluri:
 


- Ora și data la care a fost creat certificatul
- ID-ul titlului
- Numele titlului
- ID-uri alternative de titlu
- Tipuri de media permise de pe care executabilul poate fi rulat (HD, DVD, CD etc.)
- Regiunea jocului
- Evaluări ale jocului
- Numărul discului
- Versiune
- Date brute ale cheii LAN utilizate pentru System Link
- Date brute ale cheii de semnătură (utilizate pentru a semna jocurile de salvare)
- Chei alternative de semnătură
- Mărimea originală a certificatului
- Numele serviciului online (nu este prezent în executabilele timpurii)
- Indicatori de securitate pentru timpul de execuție (nu sunt prezente în executabilele timpurii)
 


### Tipuri media permise
Tipuri de media din care executabilul permite rularea. Se cunosc următoarele valori:
| Tip media | Valoare |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Secțiuni
Secțiunile sunt exprimate prin anteturile secțiunilor. Antetele secțiunilor încep imediat după certificat și conțin informații unde în fișier există secțiunile reale. Cel puțin două secțiuni sunt întotdeauna prezente într-un executabil Xbox:


- .text


- .rdata


## Referințe



* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)


