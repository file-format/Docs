{
  "date": "2021-07-13",
  "keywords": [
"CER",
"udvidelse",
"fil",
"format",
"web",
"certifikat",
"Sprog"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER - Certifikatfilformat",
  "description": "Lær om CER-filformater og API'er, der kan oprette og åbne CER-filer.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-dar"
}
},
  "lastmod": "2021-07-13"
}

## Hvad er en CER fil? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. De specifikt sikrede certifikatmyndigheder er dem, der tilhører HTTPS, en pålidelig og sikret protokol til browsing  
CER er et certifikat for din server. Det modtages normalt af certifikatmyndigheden for domænet. CER anses for det meste som det samme som [CRT](/web/crt/), selvom begge har samme format af SSL-certifikat, men er forskellige filnavne.
Disse kan bruges på operativsystemer ved blot at åbne en browser og tjekke sikkerheden for den browser eller hjemmeside, der bruges.

## Kort historie ##

I 1995 blev Thawte den første certificeringsmyndighed til at løse problemet med offentlige SSL-certifikater (secured socket link) fra USA. Derefter er der en række sådanne myndigheder, som blev grundlagt fra 1995 til 2020.

## CER-filformat ##

Disse filer kan være enkelt
* PKC S#7 omfatter Base64 ASCII-kodning
* Dens filtypenavne er p7b eller p7cZ
* For binært indhold vil certifikatet være DER eller pkcs12/pfx.
Der er mange typer certifikatfiler med nogle unikke specifikationer:
* .pem, når en organisation usThawteificate kæder dette format er velkendt for at skabe certifikater
* .arm, når metoden til at udtrække en certificering hjælper selvsigneret, er påkrævet, er det specificerede format til dette formål .arm. Det er repræsenteret i base-64 ASCII-kodning.
* .der, Den består af binære data. Det betyder, at den kun kan bruges til et enkelt certifikat
* .pfx (PKC512), Den består af en privat nøgle svarende til et certifikat udstedt af CA eller et selvsigneret certifikat. Dette format er velkendt for konvertering af den ene SSL-implementering til den anden.


