{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "fișier asmx", "format fișier asmx", "tip fișier asmx", "fișier", "tip", "ce este un fișier asmx"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - Fișier serviciu web ASP.NET",
  "description" :"Aflați despre ce este un fișier ASMX și API-urile care pot crea și deschide fișiere ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Ce este un fișier ASMX?

Un fișier cu extensii .asmx este un fișier ASP.NET Web Service care asigură comunicarea între două obiecte prin internet folosind protocolul SOAP (Simple Object Access Protocol). Este implementat ca serviciu pe serverul web bazat pe Windows pentru a procesa cererea primită și a returna răspunsul. Spre deosebire de fișierele [ASPX](/ro/web/aspx/) care conțin codul pentru afișarea vizuală a paginilor web ASP.NET, fișierele ASMX rulează pe server în fundal și efectuează diferite sarcini, cum ar fi conectarea la baza de date, preluarea datelor și returnarea acestora în un format în care a fost făcută cererea. Acestea sunt utilizate special pentru serviciile web XML.

## Format de fișier ASMX

Fișierele ASMX sunt în format text simplu și pot fi deschise sau editate în aplicații precum Microsoft Visual Studio sau editori de text. Este un format de fișier proprietar al Microsoft și are o sintaxă bine definită pentru crearea de servicii web. Un răspuns al unui fișier ASMX sub formă de SOAP XML are următoarele elemente.

* `Envelop` - Un element rădăcină care identifică documentul XML ca mesaj SOAP.
* `Header` - Un element opțional care conține informații specifice aplicației, cum ar fi datele de autentificare. Dacă elementul Header este prezent, acesta trebuie să fie primul element copil al elementului Envelope.
* `Body` - Conține mesajul SOAP destinat destinatarului.
* `Fault` - Un element opțional care este folosit pentru a indica mesajele de eroare. Dacă elementul Fault este prezent, acesta trebuie să fie un element copil al elementului Body.

Fișierele ASMX pot fi scrise în limbaje .NET, cum ar fi [C#](/ro/programming/cs/), [Visual Basic](/ro/programming/vb/) sau JScript.

## Cum este ASMX diferit de ASPX și ASCX?

Fișierele ASMX sunt diferite de fișierele ASPX și ASCX.

* ASPX, Active Server Pages, fișierele sunt fișiere de programare care sunt generate folosind framework-ul Microsoft ASP.NET care rulează pe servere web. Acestea sunt redate în browserul web al clientului atunci când utilizatorul solicită accesul la o astfel de pagină.
* ASCX, Active Server User Control, definește controalele utilizatorului care sunt utilizate pentru a defini controale reutilizabile în paginile web ASP.NET sau întregul site web.

## Referințe

* [Consumând serviciul ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Control utilizator ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

