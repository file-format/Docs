{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Aflați despre formatul de fișier CSPROJ și despre API-urile care pot crea și deschide fișiere CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Ce este un fișier CSProj?
Fișierele cu extensia CSPROJ reprezintă un fișier de proiect C# care conține lista fișierelor incluse într-un proiect împreună cu referințele la ansambluri de sistem. Când un nou proiect este inițiat în Microsoft VIiual Studio, obțineți un fișier .csproj împreună cu fișierul soluției principale ([.sln](/ro/programming/sln/)). Dacă există mai multe ansambluri într-un proiect, va exista un număr egal de fișiere de proiect, de asemenea, unde fișierul .sln le leagă pe toate ca parte a proiectului. Conținutul acestui fișier definește toate cerințele care sunt necesare pentru construirea proiectului, cum ar fi conținutul de inclus, cerințele platformei, informațiile de versiune, setările serverului web sau ale serverului de baze de date și sarcinile care trebuie efectuate. Conținutul unui fișier de proiect este aranjat în format de fișier XML și poate fi deschis în orice editor de text pentru editare și vizualizare. De asemenea, oferă o vedere logică a fișierelor de proiect pentru aranjarea corectă.

## Format fișier CSPROJ #

Dezvoltatorii pot crea fișiere de proiect singuri și respectând [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). Structura deschisă și transparentă a fișierelor de proiect permite dezvoltatorilor de aplicații să impună un control sofisticat și precis asupra modului în care proiectele sunt construite și implementate. Conținutul unui astfel de fișier de proiect are o relație foarte clară între ele. Figura următoare prezintă elemente cheie și relația dintre acestea pentru un astfel de fișier de proiect.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Următoarele secțiuni elaborează elementele de format de fișier pentru un fișier de proiect.

### Element de proiect ###

Elementul [Proiect](https://msdn.microsoft.com/library/bcxfsh87.aspx) este elementul rădăcină al fiecărui fișier de proiect. Identifică schema XML pentru fișierul de proiect și poate include atribute pentru a specifica punctele de intrare pentru procesul de construire.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Proprietăți și condiții

Proprietățile reprezintă informațiile necesare pentru a construi un proiect. Astfel de proprietăți sunt definite într-un element [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Aceste proprietăți constau din perechi cheie-valoare în care numele elementului de proprietate definește cheia de proprietate și conținutul elementului definește valoarea proprietății. De exemplu, puteți defini proprietăți numite ServerName și ConnectionString pentru a stoca un nume de server static și șir de conexiune.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Condițiile pot fi specificate prin elemente pentru a specifica criteriile de evaluare a elementului. Acest lucru este specificat de cuvântul Condiție în timp ce definiți proprietatea după cum se arată mai jos:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Când MSBuild procesează această definiție a proprietății, mai întâi verifică dacă este disponibilă o valoare a proprietății **$(OutputRoot)**. Dacă valoarea proprietății este goală - cu alte cuvinte, utilizatorul nu a furnizat o valoare pentru această proprietate - condiția este evaluată la **true**, iar valoarea proprietății este setată la **..\Publish\Out.**

### Articole și grupuri de articole

Un fișier de proiect definește intrări în procesul de construire care sunt de fapt diferite tipuri de fișiere. În nomenclatura MSBuild, aceste intrări sunt reprezentate de elemente Item și sunt definite într-un element [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). La fel ca elementele **Proprietate**, puteți denumi un element **Articol** așa cum doriți. Cu toate acestea, trebuie să specificați un atribut **Include** pentru a identifica fișierul sau wildcard pe care îl reprezintă elementul.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Ținte și sarcini

Un element [Sarcina](https://msdn.microsoft.com/library/77f2hx1s.aspx) reprezintă o instrucțiune (sau sarcină) de construire individuală. MSBuild include o multitudine de sarcini predefinite. De exemplu:

* Sarcina **Copiere** copiază fișierele într-o locație nouă.
* Sarcina **Csc** invocă compilatorul Visual C#.
* Sarcina **Vbc** invocă compilatorul Visual Basic.
* Sarcina **Exec** rulează un program specificat.
* Sarcina **Mesaj** scrie un mesaj unui logger.

Sarcinile trebuie să fie întotdeauna conținute în elementele [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Un element **Target** este un set de una sau mai multe sarcini care sunt executate secvenţial, iar un fişier proiect poate conţine mai multe ţinte.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referințe

* [Înțelegerea fișierului de proiect - MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fişier)

