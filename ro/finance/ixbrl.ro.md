{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","fișier ixbrl", "format fișier ixbrl", "tip fișier ixbrl", "fișier", "tip", "ce este un fișier ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL – Format de fișier de raportare financiară și de afaceri",
  "description":"Aflați despre formatul de fișier IXBRL și despre API-urile care pot crea și deschide fișiere IXBRL.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Ce este un fișier iXBRL?

Formatul de fișier iXBRL (ilnine XBRL) permite ca datele [XBRL](/ro/web/xbrl/) să fie încorporate într-un fișier HTML pentru a-l face atât citibil de mașină, cât și de om. Este de fapt un fișier [xHTML](/ro/web/xhtml/) care folosește etichetele XBRL și a fost dezvoltat de XBRL International pentru a îndeplini cerințele HMRC din Marea Britanie. Folosind iXBRL, situațiile financiare pot fi create păstrând intactă aspectul documentului original. Fișierele iXBRL pot fi deschise în orice editor de text, cum ar fi Notepad pe sistemul de operare Windows și TextEdit pe MacOS.

## Format de fișier iXBRL

În interiorul iXBRL, conținutul XBRL este împachetat în format de fișier xHTML care utilizează etichete XML. Ca și XBRL,<xbrl> este elementul rădăcină al fișierelor iXBRL. Formatul XHTML reprezintă conținutul său ca o colecție de diferite tipuri de documente și module. Toate fișierele din XHTML se bazează pe format de fișier XML și sunt conforme cu standardele documentelor XML. XHTML este formatul de utilizare esențială pentru utilizarea operațională a [HTML](/ro/web/html/) Document Object Model (DOM) dependent sau a [XML](/ro/web/xml/) Document Object Model. Pentru lumea exterioară, iXBRL urmează specificațiile de format de fișier [xHTML](/ro/web/xhtml/).

### iXBRL vs XBRL

XBRL poate fi comparat cu iXBRL pe baza următorilor factori:

* Complexitate
* Opțiuni de formatare
* Tipuri de fișiere/extensii
* Opțiune de randare
* Procesul de depunere

Următorul tabel ilustrează aceste diferențe.

|Parametru|XBRL|iXBRL|
---|---|---|
|Complexitate|Mai complex decât iXBRL|Mai puțin complex datorită schemei de organizare existente a XHTML|
|Opțiuni de formatare|Flexibilitate limitată|Flexibilitate ridicată pentru formatarea conținutului|
|Tipuri de fișiere/Extensie|Salvate oficial cu extensia .xml|Salvate de obicei ca extensie .html sau .xhtml|
|Opțiuni de randare|Vizualizatori XBRL sunt necesari pentru a vizualiza aceste|Conținut citibil de oameni care poate fi vizualizat în browsere|
|Proces de depunere| Documentele de instanță XBRL (lizibile de mașină) și HTML (lizibile de către oameni) care urmează să fie depuse separat.|Atât formatele care pot fi citite de către oameni, cât și cele care pot fi citite de mașină sunt disponibile într-un singur document de instanță|

## Referințe

* [XBRL - După Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

