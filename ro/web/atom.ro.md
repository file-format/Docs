{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier ATOM - Format de sindicare Atom",
  "description" :"Aflați despre ce este un fișier ATOM și API-urile care pot crea și deschide fișiere ATOM.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Ce este un fișier ATOM?

Un fișier ATOM este un format de sindicare pentru structura fluxului Atom și a documentelor de intrare. Similar cu fișierele .RSS, formatul de fișier ATOM este un format de sindicare bazat pe XML, care este un standard pentru publicarea conținutului. Un fișier ATOM este utilizat pentru fluxurile web care permit programelor software să verifice actualizările care sunt publicate pe site-ul web. Conține intrări care pot fi de diferite tipuri, cum ar fi titluri, articole cu text integral, fragmente sau link-uri către conținutul de pe un site web

Aplicațiile care pot **deschide fișierele ATOM** includ **Apple Safari**.

## Format de fișier ATOM - Mai multe informații

Fișierele ATOM sunt stocate și publicate în formatul popular de fișier XML, care este un format universal pentru schimbul de informații. A fost dezvoltat ca o alternativă la RSS ținând cont de limitările și defectele formatului de fișier RSS.

### Tipuri de documente Atom

1. `Atom Entry Documents` - Este un document XML care constă dintr-un singur element de informație, cunoscut sub numele de intrare, pentru fluxul Atom. Are un<atom:entry> element care conține un număr de elemente copil. Conținutul unei intrări Atom poate fi text simplu, HTML, XHTML sau alt tip media IANA (Internet Assigned Numbers Authority).
1. `Atom Feed Documents` - Este un document XML care furnizează metadate despre un feed Atom și una sau mai multe intrări pentru feed. Când un client face o cerere de informații din feed, documentul de feed este generat de server care include un număr de intrări Atom pentru a îndeplini cererea.
1. „Colecția Atom” - Este un tip special de document de feed Atom care conține adresele URL ale intrărilor Atom care sunt disponibile pentru a fi editate.

## Referințe

* [Atom Syndication Format - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Prezentare generală asupra Atom Feeds - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))

