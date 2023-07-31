{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Scopri il formato di file SLN e le API che possono creare e aprire file SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è il file SLN?
Un file con estensione .SLN rappresenta un file **Soluzione Visual Studio** che conserva le informazioni sull'organizzazione dei progetti in un file di soluzione. I contenuti di tale file di soluzione sono scritti in testo normale all'interno del file e possono essere osservati/modificati aprendo il file in qualsiasi editor di testo. Le informazioni contenute in un file di soluzione rimangono persistenti e vengono utilizzate per caricare le informazioni associate alla soluzione come [projects ](/it/programming/csproj/) e qualsiasi altra informazione richiesta. I file di progetto a cui fa riferimento il file di soluzione contengono informazioni aggiuntive per consentire all'ambiente di popolare la gerarchia con gli elementi di quel progetto. Nessun dato viene memorizzato nel file .sln, sebbene le informazioni sul progetto possano essere scritte nel file .sln, se necessario.

## **Cronologia versioni SLN** ##

La versione del formato della soluzione si è evoluta con ogni soluzione di Microsoft Visual Studio con il passare del tempo. I dettagli su questi sono i seguenti.


|Versione Visual Studio|Versione formato soluzione
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Contenuto di un file di soluzione** ###

Un file di soluzione è costituito da diverse sezioni che vengono lette dall'ambiente per caricare il progetto. Un esempio di contenuto del file .sln è mostrato di seguito.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Dichiarazione di progetto** ###

Un file di soluzione può contenere più di una dichiarazione di progetti e anche quella di tipi di progetto diversi. Ad esempio, un singolo file di soluzione può contenere un CSharp e un progetto VB.NET. Questi tipi vengono distinti in una soluzione utilizzando [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). La dichiarazione di progetto di cui sopra può essere generalizzata come segue per una chiara comprensione.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Il Project-Type-GUID è unico per diversi tipi di progetto e viene utilizzato dal lettore di soluzioni per identificare il tipo di progetto. In questo caso, F184B08F-C81C-45F6-A57F-5ABD9991F28F mostra che si tratta di un progetto VB.NET.

`Project GUID:` Il GUID univoco del progetto che lo differenzia da altri progetti nella soluzione. L'ID univoco di un progetto nella soluzione consente ad altri progetti nella soluzione di accedervi.

In base alle informazioni contenute nella sezione del progetto del file .sln, l'ambiente carica ogni file di progetto. Il progetto stesso è quindi responsabile del popolamento della gerarchia del progetto e del caricamento di eventuali progetti nidificati. Eventuali modifiche apportate alla soluzione vengono salvate nel file della soluzione al salvataggio o alla chiusura del progetto.

## Soluzione di Visual Studio vs progetto

**Progetto:** Logicamente, quando inizi a creare un'app o un software usando Visual Studio, inizi un nuovo progetto. Un progetto contiene tutti i file necessari come codice sorgente, icone, immagini, file di dati e altro, che verranno compilati in un'app eseguibile, un sito Web o una libreria.

**Soluzione:** una soluzione contiene uno o più progetti. Quindi la soluzione è proprio come un contenitore per i progetti di Visual Studio. Logicamente, possiamo dire che qualcuno vuole ottenere una soluzione completa per la sua attività che includa un sito Web, un'app desktop, un servizio riposante e un'app mobile.

### **Riferimenti** ###

* [File di soluzione - Da MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID del tipo di progetto](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

