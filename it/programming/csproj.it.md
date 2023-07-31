{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Scopri il formato di file CSPROJ e le API che possono creare e aprire file CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Che cos'è un file CSProj?
I file con estensione CSPROJ rappresentano un file di progetto C# che contiene l'elenco dei file inclusi in un progetto insieme ai riferimenti agli assembly di sistema. Quando un nuovo progetto viene avviato in Microsoft VIiual Studio, ottieni un file .csproj insieme al file della soluzione principale ([.sln](/it/programming/sln/)). Se ci sono più assembly in un progetto, ci sarà lo stesso numero di file di progetto anche dove il file .sln li lega tutti insieme come parte del progetto. Il contenuto di questo file definisce tutti i requisiti necessari per creare il progetto, come il contenuto da includere, i requisiti della piattaforma, le informazioni sul controllo delle versioni, le impostazioni del server Web o del server di database e le attività che devono essere eseguite. I contenuti di un file di progetto sono organizzati in formato file XML e possono essere aperti in qualsiasi editor di testo per la modifica e la visualizzazione. Fornisce inoltre una visualizzazione logica dei file di progetto per una corretta disposizione.

## Formato file CSPROJ #

Gli sviluppatori possono creare file di progetto da soli e rispettare lo [schema XML MSBuild](https://msdn.microsoft.com/library/5dy88c2e.aspx). La struttura aperta e trasparente dei file di progetto consente agli sviluppatori di applicazioni di imporre un controllo sofisticato e dettagliato sulla modalità di creazione e distribuzione dei progetti. I contenuti di un tale file di progetto hanno una relazione molto chiara tra loro. La figura seguente mostra gli elementi chiave e la relazione tra questi per un tale file di progetto.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Le sezioni seguenti elaborano gli elementi del formato file per un file di progetto.

### Elemento del progetto ###

L'elemento [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) è l'elemento radice di ogni file di progetto. Identifica lo schema XML per il file di progetto e può includere attributi per specificare i punti di ingresso per il processo di compilazione.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Proprietà e condizioni

Le proprietà rappresentano le informazioni necessarie per costruire un progetto. Tali proprietà sono definite all'interno di un elemento [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Queste proprietà sono costituite da coppie chiave-valore in cui il nome dell'elemento della proprietà definisce la chiave della proprietà e il contenuto dell'elemento definisce il valore della proprietà. Ad esempio, è possibile definire proprietà denominate ServerName e ConnectionString per archiviare un nome server statico e una stringa di connessione.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Le condizioni possono essere specificate tramite elementi per specificare i criteri per la valutazione dell'elemento. Questo è specificato da Parola condizione durante la definizione della proprietà come mostrato di seguito:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Quando MSBuild elabora questa definizione di proprietà, verifica innanzitutto se è disponibile un valore di proprietà **$(OutputRoot)**. Se il valore della proprietà è vuoto, in altre parole, l'utente non ha fornito un valore per questa proprietà, la condizione restituisce **true** e il valore della proprietà è impostato su **..\Publish\Out.**

### Articoli e gruppi di articoli

Un file di progetto definisce gli input per il processo di compilazione che sono in realtà tipi di file diversi. Nella nomenclatura MSBuild, questi input sono rappresentati da elementi Item e sono definiti all'interno di un elemento [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Proprio come gli elementi **Proprietà**, puoi nominare un elemento **Elemento** come preferisci. Tuttavia, devi specificare un attributo **Include** per identificare il file o il carattere jolly rappresentato dall'elemento.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Obiettivi e attività

Un elemento [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) rappresenta una singola istruzione (o attività) di compilazione. MSBuild include una moltitudine di attività predefinite. Per esempio:

* L'attività **Copia** copia i file in una nuova posizione.
* L'attività **Csc** richiama il compilatore Visual C#.
* L'attività **Vbc** richiama il compilatore di Visual Basic.
* L'attività **Exec** esegue un programma specifico.
* L'attività **Messaggio** scrive un messaggio in un logger.

Le attività devono sempre essere contenute negli elementi [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Un elemento **Target** è un insieme di una o più attività eseguite in sequenza e un file di progetto può contenere più destinazioni.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Riferimenti

* [Capire il file di progetto - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- file)

