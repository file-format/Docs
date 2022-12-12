{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier MDMP - Format de fișier Windows Minidump",
  "description":"Aflați despre formatul de fișier MDMP și despre API-urile care pot crea și deschide fișiere MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Ce este un fișier MDMP?

Un fișier MDMP este o descărcare de memorie a unei aplicații pe Microsoft Windows care este creată atunci când aplicația se închide anormal sau se blochează. Conține informații și depozite de date care pot fi utilizate pentru a depana cauza accidentului. Fișierele MDMP sunt aplicabile pe aplicațiile create de orice platformă, cum ar fi Java, C++, .NET și altele. Pe lângă MDMP,

Aplicațiile care pot deschide fișiere MDMP includ Microsoft Visual Studio Debugger.

## Format de fișier MDMP

Fișierele MDMP sunt salvate ca fișiere binare pe disc și pot fi deschise cu Microsoft Visual Studio debugger. Conține următoarele informații pentru a ajuta la identificarea motivului accidentului.

* Detalii despre mesajul Stop, parametrii acestuia și alte date
* Lista driverelor încărcate
* Contextul procesorului (PRCB) pentru procesorul care a încetat să funcționeze
* Informații despre proces și contextul kernelului (EPROCESS) pentru procesul care s-a oprit
* Informații de proces și contextul kernelului (ETHREAD) pentru firul care s-a oprit
* Stiva de apeluri în modul kernel pentru firul care s-a oprit

Aceste informații vă ajută să aflați ce s-a întâmplat, să remediați problema și să împiedicați să se repete.

### Analizați Minidump

Windows necesită un fișier de paginare pe volumul de pornire pentru a crea un fișier de descărcare a memoriei. Fișierul de paginare este creat pe volumul de pornire și ar trebui să aibă o dimensiune de cel puțin 2 megaocteți (MB). Fișierul dump este creat atunci când o aplicație se blochează. În cazul unei a doua probleme, este creat un al doilea fișier mic de descărcare a memoriei, în timp ce cel anterior este păstrat. Numele fișierului dump este distinct pentru a evita orice suprascriere.

Windows păstrează o listă cu toate fișierele de descărcare a memoriei din folderul %SystemRoot%\Minidump. Puteți analiza fișierele MDMP rulându-le în Visual Studio Debugger, așa cum este listat în pașii de mai jos.

## Cum deschid un fișier MDMP în Visual Studio?

Următorii pași pot fi utilizați pentru a deschide un fișier MDMP în Visual Studio.

* În Visual Studio, din meniul Fișier, alegeți Deschidere | Crash Dump .
* Navigați la fișierul dump pe care doriți să îl deschideți.
* Selectați Deschidere.

## Referinţă

* [Cum să citiți fișierul mic de descărcare a memoriei care este creat de Windows dacă are loc o blocare](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fişier)

