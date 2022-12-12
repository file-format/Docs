{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "format fișier", "tip fișier", "ce este un fișier .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Fișier de configurare ASP",
  "description" :"Aflați despre ce este un fișier ASA și API-urile care pot crea și deschide fișiere ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Ce este un fișier ASA?

Un fișier ASA este un fișier de configurare, creat pentru proiecte [ASP](/ro/web/asp/)/ASP.NET. Conține declarații de variabile, conține și funcții care sunt menite să fie accesibile la nivel global în aplicație. Toate paginile din proiect pot accesa aceste variabile și funcții, evitând astfel necesitatea rescrierii acestora. Un astfel de exemplu este pagina Global.asa care este stocată în directorul rădăcină pentru a fi accesibilă de către alte pagini ale site-ului ASP. Fișierele Global.asa sunt opționale, dar dacă sunt utilizate, fiecare aplicație poate avea un singur fișier Global.asa.

## Format de fișier ASA - Mai multe informații

Fișierele ASA sunt fișiere text simplu cu următoarele informații.

* Evenimente de aplicație
* Evenimente de sesiune
* \<object> declarații
* Declarații TypeLibrary
* directiva #include

## Exemplu de fișier ASA

Un fișier Global.asa ar putea arăta cam așa.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referințe

* [Fișier ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

