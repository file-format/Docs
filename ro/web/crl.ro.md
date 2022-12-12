{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier CRL - Listă de revocare a certificatelor",
  "description":"Aflați despre formatul fișierului CRL și despre API-urile care pot crea și deschide fișiere CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Ce este un fișier CRL?

Un fișier CRL (Certificate Revocation List) este o listă neagră de certificate digitale X.509 pe care o autoritate de certificare (CA) le revocă înainte de data de revocare atribuită. Conține informații despre problemă și data revocării care le permite administratorilor de securitate să blocheze certificatele digitale afectate. CRL nu include certificate expirate, deoarece scopul său principal este de a notifica despre certificatele care nu sunt de încredere și nevalide.

Aplicațiile care pot **deschide fișierele CRL** includ OpenSSL, Microsoft IIS Server și Citrix NetScaler.

## Format fișier CRL - Mai multe informații

Fișierele CRL conțin informații în standardul X.509 care își definește și semantica pentru partajarea informațiilor cheie publice. Alte informații conținute într-un fișier CRL pot include limita de timp pentru care certificatele au fost revocate, motivul revocării, numărul de serie al certificatului revocat și marca temporală.


### Principalele motive pentru care certificatele sunt adăugate la CRL

Ar putea exista mai multe motive pentru a obține revocarea certificatului site-ului dvs. și pentru a fi adăugat la CRL. Unele dintre ele ar putea fi;

1. Cheia privată a certificatului dvs. a fost compromisă
1. Certificatul dumneavoastră nu este valid sau eliberat greșit de CA
1. Detaliile organizaționale asociate cu certificatul sunt modificate și CA emite un nou certificat
1. Orice alt motiv inevitabil pentru care certificatul a fost revocat

## Referințe

* [Institutul Național de Standarde și Tehnologie (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force's (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Lista de revocare a certificatelor](https://en.wikipedia.org/wiki/Certificate_revocation_list)

