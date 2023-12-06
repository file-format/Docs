{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier AXD - Format fișier ASP.NET Web Handler",
  "description" :"Aflați despre ce este un fișier AXD și API-urile care pot crea și deschide fișiere AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Ce este un fișier AXD?

Un fișier AXD este un fișier de setări web care este utilizat pentru gestionarea și recuperarea cererilor de resurse încorporate în ASP.NET. Acesta cuprinde instrucțiuni pentru recuperarea resurselor încorporate, cum ar fi imagini, fișiere JavaScript ([.JS](/ro/web/js/)) și fișiere [.CSS](/ro/web/css/). Fișierele AXD sunt folosite pentru a injecta resurse în paginile clientului. Acest lucru permite paginilor client să acceseze aceste resurse pe server într-un mod standard.

## Format de fișier AXD

Fișierele AXD sunt stocate ca fișiere binare pe partea serverului. Se referă la un fișier Web Handler din ASP.NET care sunt componente care generează răspunsuri la cereri specifice către un server web. Fișierele AXD efectuează procesare personalizată înainte de a genera răspunsul bazat pe solicitările paginii client. Acestea sunt de obicei salvate ca fișiere **WebResource.axd**.

### Ce este fișierul WebResource.axd?

Majoritatea proiectelor ASP.NET salvează fișierele AXD ca fișiere WebResource.axd, care permit paginilor clientului să descarce resurse care sunt încorporate într-un ansamblu. Aplicația dvs. se poate confrunta cu o performanță lentă în cazul în care o rulați în modul de depanare, deoarece handlerul WebResources.axd nu este stocat în cache.

## Referințe

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

