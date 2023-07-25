{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","fișier ascx", "format fișier ascx", "tip fișier ascx", "fișier", "tip", "ce este un fișier ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ASCX",
  "description" :"Aflați despre ce este un fișier ASCX și API-urile care pot crea și deschide fișiere ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier ASCX?

Un fișier cu extensia .ascx este un control de utilizator care este utilizat ca componentă reutilizabilă în paginile web. Este referit în orice site web ASP trăgându-l din caseta de control în pagină. Controalele utilizatorilor ASCX sunt adăugate la proiect ca sursă centrală, ceea ce duce la orice modificare a controlului utilizatorului care se reflectă pe întregul site web. Spre deosebire de fișierele ASMX care definesc un mecanism de comunicare în cadrul a 2 obiecte prin internet, fișierele ASCX sunt comenzi de utilizator pentru încorporarea în pagini sau site-uri web.

## Format de fișier ASCX

Fișierele ASCX sunt scrise în format text simplu și pot folosi codul din spatele funcțiilor precum paginile web care se termină cu .ascx.cs. Codul de marcare al comenzilor utilizatorului începe cu directiva @Control, așa cum se arată în exemplul următor.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Acest control al utilizatorului web poate fi reutilizat pe multe pagini, cum ar fi subsolul paginii, antetul sau un fel de navigare pe site. Controalele utilizatorilor web au proprietăți, metode și evenimente ca orice alt control, care le fac utile în stabilirea comportamentului lor vizual.

### Exemplu de înregistrare a comenzilor utilizatorului în web.config

Pentru a utiliza un singur control utilizator pe mai multe pagini, controlul web poate fi înregistrat în web.config. Acest lucru vă permite să utilizați controlul asupra întregului site web în loc să vă înregistrați pe fiecare pagină individual. Următorul cod exemplu definește modul de înregistrare a unui control web în web.config pentru a fi afișat ca subsol pe întregul site web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Referințe

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [Control utilizator ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

