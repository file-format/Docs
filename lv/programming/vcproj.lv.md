{
  "date": "2023-05-15",
  "keywords": [
"vcproj failu",
"kas ir vcproj fails",
"vcproj faila piemērs",
"ko satur vcproj fails",
"kāds ir vcproj faila formāts",
"failu",
"vcproj faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VCPROJ faila formāts — Visual C++ projekta fails",
  "description": "Uzziniet par VCPROJ formātu un API, kas var izveidot un atvērt VCPROJ failus.",
  "linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## Kas ir VCPROJ fails?

A VCProj file, also known as Visual C++ Project file, is an XML-based file that stores configuration and settings for project in Microsoft Visual Studio. VCProj files are primarily used in older versions of Visual Studio, up to Visual Studio 2010. Sākot ar Visual Studio 2012, projekta faili tika mainīti uz jaunu formātu ar nosaukumu VCXProj.

VCProj fails satur informāciju par projekta avota koda failiem, būvējuma iestatījumiem, kompilatora opcijām, linkera iestatījumiem un citām projekta konfigurācijām. Tas nosaka, kā projekts tiek veidots un kādi faili ir iekļauti projektā.

## VCPROJ faila piemērs

Šeit ir piemērs tam, kā varētu izskatīties VCProj fails:

```
<?xml version="1.0" encoding="Windows-1252"?>
<VisualStudioProject
	ProjectType="Visual C++"
	Version="9.00"
	Name="MyProject"
	ProjectGUID="{01234567-89AB-CDEF-0123-456789ABCDEF}"
	Keyword="Win32Proj"
	>
	<Platforms>
		<Platform
			Name="Win32"
		/>
	</Platforms>
	<ToolFiles>
	</ToolFiles>
	<Configurations>
		<Configuration
			Name="Debug|Win32"
			ConfigurationType="1"
			InheritedPropertySheets="$(VCInstallDir)VCProjectDefaults\UpgradeFromVC71.vsprops"
		>
			<Tool
				Name="VCCLCompilerTool"
				AdditionalIncludeDirectories=".\include"
				PreprocessorDefinitions="_DEBUG;WIN32;_WINDOWS"
				RuntimeLibrary="3"
				UsePrecompiledHeader="0"
			/>
			<Tool
				Name="VCLinkerTool"
				AdditionalDependencies="kernel32.lib user32.lib"
				OutputFile="$(OutDir)\MyProject.exe"
				LinkIncremental="2"
				SuppressStartupBanner="true"
			/>
		</Configuration>
	</Configurations>
	<References>
	</References>
</VisualStudioProject>

```

## Ko satur VCPROJ fails?

VCProj failā ir dažādi elementi un iestatījumi, kas saistīti ar Visual C++ projektu programmā Microsoft Visual Studio. Šeit ir daži no galvenās informācijas, ko var atrast VCProj failā:

- **Project Information:** The VCProj file includes project-level information such as the project name, project type, version, and unique identifier (GUID) for the projec-lvt.
- **Platformas un konfigurācijas:** norāda projekta atbalstītās platformas un konfigurācijas. Platformas nosaka mērķa platformu, piemēram, Win32, x64 vai ARM, savukārt konfigurācijas nosaka dažādas būvēšanas konfigurācijas, piemēram, atkļūdošana vai izlaišana.
- **Avota faili:** VCProj failā ir uzskaitīti avota koda faili, kas ir daļa no projekta, tostarp C++ faili, galvenes faili, resursu faili un citi saistītie faili. Katrs fails parasti ir norādīts ar tā relatīvo ceļu uz projekta direktoriju.
- **Būvējuma iestatījumi:** tajā ir iekļauti iestatījumi, kas saistīti ar veidošanas procesu, piemēram, kompilatora opcijas, linkera opcijas, priekšprocesora definīcijas, papildu iekļaušanas direktoriji un papildu atkarības. Šie iestatījumi nosaka, kā projekts ir izveidots un saistīts.
- **Iepriekš kompilētas galvenes:** VCProj fails var norādīt, vai projektā tiek izmantotas iepriekš kompilētas galvenes, un, ja tā, tad kurš fails kalpo kā iepriekš kompilētā galvene.
- **Izvades informācija:** tā nosaka izvades failu vai failus, ko ģenerē veidošanas process, piemēram, izpildāmo failu, dinamisko saišu bibliotēku (DLL) vai statisko bibliotēku (LIB). Izvades faila ceļu un nosaukumu var konfigurēt VCProj failā.
- **Atsauces:** VCProj failā var būt atsauces uz citiem projektiem vai ārējām bibliotēkām, no kurām projekts ir atkarīgs. Šīs atsauces palīdz atrisināt atkarības veidošanas procesa laikā.
- **Pielāgotas izveides darbības:** ja projektam ir nepieciešamas papildu pielāgotas veidošanas darbības, piemēram, skriptu palaišana vai ārēju rīku izpilde, VCProj failā var būt ietverti norādījumi par šīm darbībām.
- **Atkļūdošana un izvietošana:** VCProj failā var būt ietverti iestatījumi, kas saistīti ar atkļūdošanu, izvietošanu un citām projektam specifiskām konfigurācijām.

## Kāds ir VCPROJ faila formāts?

VCProj faila formāts ir balstīts uz XML (eXtensible Markup Language), kas ir standarta iezīmēšanas valoda strukturētu datu attēlošanai. XML formāts ļauj organizēt un uzglabāt projektam specifisku informāciju un iestatījumus hierarhiskā struktūrā.

## Atsauces
* [Projektu un risinājumu faili](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)


