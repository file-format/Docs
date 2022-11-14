{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "estensione", "formato file", "Progetto Visual C++", "Guida alla programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Scopri il formato di file VCXPROJ e le API che possono creare e aprire file VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file VCXPROJ?

Un file con estensione .vcxproj è un file di progetto Microsoft Visual C++ che memorizza le informazioni sul progetto [C++](/it/programming/cpp/). Contiene informazioni utilizzate dal sistema di progetto MSBuild per compilare e creare l'output finale. VCXPROJ dei progetti di Visual C++ è uguale a quello di [CSPROJ](/it/programming/csproj/) per i progetti .NET. I file VCXPROJ non contengono alcun codice ma fanno riferimento a tutte le classi, destinazioni e proprietà definite per il progetto per creare il progetto. Questi possono essere aperti in editor di testo normale o preferibilmente in Microsoft Visual Studio IDE.


## Formato file VCXPROJ - Ulteriori informazioni

I file VCXPROJ sono file di testo creati nel formato file [XML](/it/web/xml/). Questi possono essere aperti in qualsiasi editor di testo, ma si consiglia vivamente di utilizzare Microsoft Visual Studio IDE per aprire e modificare questi file. Questi non sono stati progettati per la modifica manuale. Gli errori possono causare l'arresto anomalo dell'IDE o comportarsi in modi imprevisti.

I contenuti di un file di esempio VCXPROJ sono i seguenti.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Elementi del file VCXPROJ

Un tipico file VCXPROJ contiene un numero di elementi come si può vedere nell'esempio XML sopra. La [struttura VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) di Microsoft spiega ogni elemento del file in dettaglio e può essere referenziato dal punto di vista dello sviluppatore.

#### Elemento del progetto

Questo è il nodo principale del file VCXPROJ. MSBuild usa questo elemento per leggere la versione build e la destinazione predefinita per la compilazione.

#### Elemento ItemGroup di ProjectConfigurations

Contiene le informazioni sulla configurazione del progetto che possono includere il metodo di compilazione (debug o rilascio), la compilazione a 32 o 64 bit, le opzioni di ottimizzazione e altro. Le informazioni in questo gruppo vengono utilizzate da IDE per caricare il progetto.

#### Elementi di configurazione del progetto

Gli elementi ProjectConfiguration in un file VCXPROJ contengono informazioni sulla build e sulla piattaforma per cui viene caricato il progetto. Il suo nome dovrebbe seguire il formato `$(Configurazione)|$(Piattaforma)`.

#### Elemento PropertyGroup globali

Questa sezione contiene impostazioni che forniscono informazioni a livello di progetto come:

* Guida al progetto
* Spazio dei nomi radice
* ApplicationType o ApplicationTypeRevision


## Riferimenti

* [Struttura VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [File di progetto C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

