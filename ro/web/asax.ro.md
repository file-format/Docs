{
  "date" : "2019-10-11",
  "keywords" :[ "asax","fișier asax", "format fișier asax", "tip fișier asax", "fișier", "tip", "ce este un fișier asax"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - Fișier aplicație server ASP.NET",
  "description" :"Aflați să știți ce este un fișier ASAX și API-urile care pot crea și deschide fișiere ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Ce este un fișier ASAX?

Un fișier cu extensia .asax este un fișier utilizat de aplicațiile ASP.NET care se află pe partea serverului. Conține cod pentru a răspunde la evenimente la nivel de aplicație și la nivel de sesiune generate de ASP.NET sau de modulele HTTP. Aceasta include și gestionarea anumitor evenimente atunci când aplicația se lansează sau se închide. Fișierele ASAX sunt opționale și doar un singur fișier ASAX este adăugat la aplicațiile web pentru a gestiona evenimentele și erorile la nivel de aplicație la nivel global. Spre deosebire de paginile ASPX, fișierele ASAX nu conțin niciun cod care să implementeze funcționalitatea aplicației.

## Format de fișier ASAX

Fișierele ASAX sunt scrise în format text simplu și pot fi citite de om. Fișierul ASAX cel mai frecvent utilizat este Global.asax, care se află în directorul rădăcină al unei aplicații ASP.NET. Serverele web sunt configurate să respingă orice apeluri primite către acest fișier, pentru a le interzice utilizatorilor să descarce sau să vizualizeze codul acestui fișier.

### Global.ASAX - Un exemplu de format de fișier ASAX

Un singur fișier ASAX constă din mai multe secțiuni care sunt scrise pentru a gestiona evenimentele la nivel de aplicație. Acestea sunt după cum urmează.

* **Directive de aplicație** - Directivele de aplicație sunt etichete care sunt utilizate pentru a defini setările opționale specifice aplicației care vor fi utilizate de parserul ASP.NET atunci când procesează fișierul Global.asax. Aceste directive sunt situate la începutul fișierului Global.asax și sunt definite după cum urmează.

```
<%@ directivă atribut=valoare [atribut=valoare … ]%>
```
* **Blocuri de declarație de cod** - Blocurile de declarație de cod sunt utilizate pentru a defini secțiuni de cod de server care sunt încorporate în fișierele aplicației ASP.NET în \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - Acestea definesc codul sau expresiile inline care se execută atunci când pagina este redată. Cele două stiluri de blocuri de randare de cod includ cod inline și expresii inline. Primul este folosit pentru a defini linii autonome sau blocuri de cod, în timp ce lateral este folosit ca o comandă rapidă pentru apelarea metodei Write.

## Referințe

* [Prezentare generală a manevrelor HTTP și a modulelor HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Sintaxă Global.asax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

