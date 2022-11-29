{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Läs mer om CSPROJ-filformat och API:er som kan skapa och öppna CSPROJ-filer.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Vad är en CSProj fil?
Filer med tillägget CSPROJ representerar en C#-projektfil som innehåller listan över filer som ingår i ett projekt tillsammans med referenserna till systemsammansättningar. När ett nytt projekt initieras i Microsoft VIiual Studio får du en .csproj-fil tillsammans med huvudlösningsfilen ([.sln](/sv/programming/sln/)). Om det finns mer än en sammansättning i ett projekt, kommer det att finnas lika många projektfiler där .sln-filen binder samman dem alla som en del av projektet. Innehållet i den här filen definierar alla krav som krävs för att bygga projektet, såsom innehåll som ska inkluderas, plattformskraven, versionsinformation, webbserver- eller databasserverinställningar och de uppgifter som måste utföras. Innehållet i en projektfil är ordnat i XML-filformat och kan öppnas i valfri textredigerare för redigering och visning. Det ger också en logisk bild av projektfilerna för korrekt arrangemang.

## CSPROJ filformat #

Utvecklare kan skapa projektfiler själva och respektera [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). Den öppna och transparenta strukturen för projektfiler låter applikationsutvecklare införa sofistikerad och finkornig kontroll över hur projekten byggs och distribueras. Innehållet i en sådan projektfil har en mycket tydlig relation sinsemellan. Följande figur visar nyckelelement och förhållandet mellan dessa för en sådan projektfil.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Följande avsnitt utvecklar filformatelementen för en projektfil.

### Projektelement ###

Elementet [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) är rotelementet i varje projektfil. Den identifierar XML-schemat för projektfilen och kan inkludera attribut för att specificera startpunkterna för byggprocessen.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Egenskaper och villkor

Fastigheter representerar den information som krävs för att bygga ett projekt. Sådana egenskaper definieras i ett [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) element. Dessa egenskaper består av nyckel-värdepar där egenskapselementets namn definierar egenskapsnyckeln och innehållet i elementet definierar egenskapsvärdet. Du kan till exempel definiera egenskaper som heter ServerName och ConnectionString för att lagra ett statiskt servernamn och anslutningssträng.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Villkor kan specificeras via element för att specificera kriterierna för att utvärdera elementet. Detta specificeras av villkorsord medan egenskapen definieras enligt nedan:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

När MSBuild bearbetar den här egenskapsdefinitionen kontrollerar den först om ett egenskapsvärde **$(OutputRoot)** är tillgängligt. Om egenskapsvärdet är tomt – med andra ord, användaren inte har angett något värde för den här egenskapen – utvärderas villkoret till **true** och egenskapsvärdet sätts till **..\Publish\Out.**

### Föremål och föremålsgrupper

En projektfil definierar ingångar till byggprocessen som faktiskt är olika filtyper. I MSBuild-nomenklaturen representeras dessa indata av Item-element och definieras i ett [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx)-element. Precis som **Property**-element kan du namnge ett **Item**-element som du vill. Du måste dock ange ett **Inkludera**-attribut för att identifiera filen eller jokertecken som objektet representerar.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Mål och uppgifter

Ett [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) element representerar en individuell bygginstruktion (eller uppgift). MSBuild innehåller en mängd fördefinierade uppgifter. Till exempel:

* Uppgiften **Kopiera** kopierar filer till en ny plats.
* Uppgiften **Csc** anropar Visual C#-kompilatorn.
* **Vbc**-uppgiften anropar Visual Basic-kompilatorn.
* Uppgiften **Exec** kör ett specificerat program.
* Uppgiften **Meddelande** skriver ett meddelande till en logger.

Uppgifter måste alltid finnas i [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) element. Ett **Target**-element är en uppsättning av en eller flera uppgifter som exekveras sekventiellt, och en projektfil kan innehålla flera mål.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referenser

* [Förstå projektfilen - MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fil)

