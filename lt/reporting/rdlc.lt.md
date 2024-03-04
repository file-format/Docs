{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDLC – ataskaitos apibrėžimo kalbos kliento pusė",
  "keywords": [
"rdlc",
"ataskaitos apibrėžimo kalba",
"mkv formatu",
"XSD",
"ataskaitos apibrėžimo kalbos kliento pusė"
],
  "description": "Sužinokite apie RDLC failo formatą, kuris yra „SQL Server Reporting Services“ ataskaitos apibrėžimo XML atvaizdas.",
  "linktitle": "RDLC",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-ltc"
}
},
  "lastmod": "2021-03-02"
}

## Kas yra RDLC failas? ##

RDLC reiškia ataskaitos apibrėžimo kalbos kliento pusę. Tiesą sakant, tai yra ataskaitos failo plėtinys, sukurtas naudojant Microsoft ataskaitų teikimo technologiją. Šiems failams kurti naudojama SQL Server 2005 versija Report Designer. **ReportViewer** valdiklis kliento pusėje gali tiesiogiai vykdyti RDLC ataskaitas.

## RDL VS RDLC failai
|.rdl failai |.rdlc failai|
---|---|
|RDL failai sukurti naudojant SQL Server 2005 Report Designer versiją|RDLC failus sukuria Visual Studio 2005 Report Designer|
|Jis naudojamas SQL Server Reporting Services|Jis naudojamas Visual Studio|
|Tai nuotolinė ataskaita|Tai vietinė ataskaita|
|Jam paleisti reikalingas Reporting Services egzempliorius|Nereikia Reporting Services egzemplioriaus|

## Kliento ataskaitos apibrėžimo (.rdlc) failų kūrimas
ReportViewer valdiklis naudojamas kliento ataskaitos apibrėžimo (.rdlc) failams paleisti naudojant įtaisytąją valdiklio apdorojimo galimybę. Kliento ataskaitas, kurias naudojate vietinio apdorojimo režimu, galite lengvai sukurti jūsų taikomosios programos projekte. Toliau pateikiami ataskaitos kūrimo būdai:

- Norėdami sukurti naują kliento ataskaitos apibrėžimą (.rdlc), naudokite **Ataskaitų vedlį**.

– Sukurkite naują kliento ataskaitos apibrėžimo (.rdlc) failą naudodami Visual Studio.

– Programiškai generuokite ataskaitos apibrėžimą.


Ataskaitą galite peržiūrėti tik paleidę ją **ReportViewer** valdiklyje. Atminkite, kad galite bet kada atidaryti ir redaguoti ataskaitos apibrėžimą, tada sukurti arba įdiegti programą, kad patikrintumėte rezultatus.

## Nuorodos Nr.

- [Creating Client Report Definition (.rdlc) Files](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

