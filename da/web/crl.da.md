{
  "date": "2022-09-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRL-fil - Liste over tilbagekaldelse af certifikater",
  "description": "Lær om CRL-filformat og API'er, der kan oprette og åbne CRL-filer.",
  "linktitle": "CRL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-dal"
}
},
  "lastmod": "2022-09-01"
}

## Hvad er CRL fil?

En CRL-fil (Certificate Revocation List) er en sortliste over X.509 digitale certifikater, som en certifikatmyndighed (CA) tilbagekalder før deres tildelte tilbagekaldelsesdato. Den indeholder oplysninger om problemet og tilbagekaldelsesdatoen, der giver sikkerhedsadministratorerne mulighed for at blokere berørte digitale certifikater. CRL inkluderer ikke udløbne certifikater, da dets hovedformål er at give besked om de ikke-pålidelige og ugyldige certifikater.

Programmer, der kan **åbne CRL-filer**, inkluderer OpenSSL, Microsoft IIS Server og Citrix NetScaler.

## CRL-filformat - flere oplysninger

CRL-filer indeholder information i X.509-standarden, som også definerer dens semantik for deling af offentlig nøgleinformation. Andre oplysninger indeholdt i en CRL-fil kan omfatte den tidsfrist, for hvilken certifikaterne er blevet tilbagekaldt, årsagen til tilbagekaldelsen, serienummeret på det tilbagekaldte certifikat og tidsstempel.


### Vigtigste årsager til, at certifikater bliver tilføjet til CRL

Der kan være flere årsager til at få dit websteds certifikat tilbagekaldt og blive tilføjet til CRL. Nogle af dem kunne være;

1. Dit certifikats private nøgle er blevet kompromitteret
1. Dit certifikat er ikke gyldigt eller forkert udstedt af CA
1. Organisationsoplysninger knyttet til certifikatet ændres, og CA udsteder nyt certifikat
1. Enhver anden uundgåelig årsag til, at certifikatet er blevet tilbagekaldt

## Referencer

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)

* [Internet Engineering Task Force's (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)

* [Certification Revocation List](https://en.wikipedia.org/wiki/Certificate_revocation_list)


