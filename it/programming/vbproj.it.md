{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "estensione", "formato file", "File progetto VB", "Guida alla programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Scopri il formato di file VBPROJ e le API che possono creare e aprire file VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file VBPROJ?

Un file con estensione .vbproj è un file di progetto di Microsoft Visual Basic che viene utilizzato dal motore MSBuild di Microsoft per creare i progetti all'interno di una soluzione di Visual Studio. È simile al file [CSPROJ](/it/programming/csproj/) per i progetti .NET scritti in [C#](/it/programming/cs/). Il motore MSBuild legge le informazioni contenute in diversi gruppi dai file VBPROJ e genera il file di output. Un file VBPROJ può contenere informazioni relative a identificatori globali, classi e proprietà che definiscono il progetto. I file VBPROJ possono essere aperti e modificati utilizzando Microsoft Visual Studio e qualsiasi editor di testo comune come Blocco note su sistemi operativi Windows e MacOS.

## Formato file VBPROJ - Ulteriori informazioni

I file VBPROJ sono file di testo scritti nel formato di file [XML](/it/web/xml/) basato su [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). Un file VBPROJ contiene informazioni sotto forma di tag XML che definiscono le informazioni relative a quel particolare gruppo di impostazioni. Si consiglia vivamente di aprire e modificare questi file di impostazione nell'IDE di Microsoft Visual Studio.

### Elementi VBPROJ

Gli elementi costitutivi di un file di impostazioni VB sono come mostrato nell'immagine seguente.

{{< figure src="../vbproj.png" alt="Formato file VBPROJ" >}}

La tabella seguente fornisce una breve descrizione di questi elementi.

|Elemento|Descrizione|
---|---|
|Progetto| Elemento radice di ogni file di progetto e può includere attributi per specificare i punti di ingresso per il processo di compilazione oltre a identificare lo schema XML per il file di progetto|
|Proprietà e condizioni| Le proprietà sono costituite da coppie chiave-valore e sono definite all'interno di un elemento PropertyGroup. Il nome dell'elemento della proprietà rappresenta la chiave della proprietà e il contenuto dell'elemento definisce il valore della proprietà.|
|Elementi e ItemGroups|Gli elementi in un file di progetto sono input per il processo di compilazione come file di codice, file di configurazione, file di comando e altri richiesti come parte del processo di compilazione. Gli elementi sono e devono essere definiti all'interno di un elemento ItemGroup.|
|Obiettivi e attività| Un elemento Task rappresenta una singola istruzione di build (o attività). MSBuild include una moltitudine di attività predefinite come Copia, CSC, VBC, Exec. Le attività devono sempre essere contenute in un elemento `Target` che è un insieme di una o più attività eseguite in sequenza e un file di progetto può contenere più destinazioni.|

## Riferimenti

* [Capire il file di progetto](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elementi dello schema MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

