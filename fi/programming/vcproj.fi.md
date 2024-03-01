{
  "date": "2023-05-15",
  "keywords": [
"vcproj tiedosto",
"mikä on vcproj-tiedosto",
"esimerkki vcproj-tiedostosta",
"mitä vcproj-tiedosto sisältää",
"mikä on vcproj-tiedoston muoto",
"tiedosto",
"vcproj tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VCPROJ-tiedostomuoto - Visual C++ -projektitiedosto",
  "description": "Opi VCPROJ-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata VCPROJ-tiedostoja.",
  "linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## Mikä on VCPROJ-tiedosto?

A VCProj file, also known as Visual C++ Project file, is an XML-based file that stores configuration and settings for project in Microsoft Visual Studio. VCProj files are primarily used in older versions of Visual Studio, up to Visual Studio 2010. Visual Studio 2012:sta alkaen projektitiedostot muutettiin uuteen muotoon nimeltä VCXProj.

VCProj-tiedosto sisältää tietoja projektin lähdekooditiedostoista, koontiasetuksista, kääntäjän vaihtoehdoista, linkkiasetuksista ja muista projektikohtaisista kokoonpanoista. Se määrittelee, miten projekti rakennetaan ja mitä tiedostoja projektiin sisältyy.

## Esimerkki VCPROJ-tiedostosta

Tässä on esimerkki siitä, miltä VCProj-tiedosto saattaa näyttää:

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

## Mitä VCPROJ-tiedosto sisältää?

VCProj-tiedosto sisältää erilaisia elementtejä ja asetuksia, jotka liittyvät Visual C++ -projektiin Microsoft Visual Studiossa. Tässä on joitain tärkeitä tietoja, jotka löytyvät VCProj-tiedostosta:

- **Project Information:** The VCProj file includes project-level information such as the project name, project type, version, and unique identifier (GUID) for the projec-fit.
- **Alustat ja kokoonpanot:** Se määrittää projektin tukemat alustat ja kokoonpanot. Alustat määrittävät kohdealustan, kuten Win32, x64 tai ARM, kun taas kokoonpanot määrittävät erilaiset koontikokoonpanot, kuten Debug tai Release.
- **Lähdetiedostot:** VCProj-tiedostossa luetellaan projektiin kuuluvat lähdekooditiedostot, mukaan lukien C++-tiedostot, otsikkotiedostot, resurssitiedostot ja muut asiaan liittyvät tiedostot. Jokaiselle tiedostolle on yleensä määritetty sen suhteellinen polku projektihakemistoon.
- **Koontiversioasetukset:** Se sisältää koontiprosessiin liittyvät asetukset, kuten kääntäjän asetukset, linkkiasetukset, esiprosessorin määritykset, lisätietohakemistot ja lisäriippuvuudet. Nämä asetukset määrittävät, miten projekti rakennetaan ja linkitetään.
- **Esikäännetyt otsikot:** VCProj-tiedosto voi määrittää, käyttääkö projekti esikäännettyjä otsikoita, ja jos on, mikä tiedosto toimii esikäännettynä otsikkona.
- **Output Information:** Se määrittää koontiprosessin tuottaman tulostiedoston tai tiedostot, kuten suoritettavan tiedoston, dynaamisten linkkien kirjaston (DLL) tai staattisen kirjaston (LIB). Tulostiedoston polku ja nimi voidaan määrittää VCProj-tiedostossa.
- **Viitteet:** VCProj-tiedosto voi sisältää viittauksia muihin projekteihin tai ulkoisiin kirjastoihin, joista projekti riippuu. Nämä viittaukset auttavat ratkaisemaan riippuvuuksia rakennusprosessin aikana.
- **Muokatut koontivaiheet:** Jos projekti vaatii muita mukautettuja koontivaiheita, kuten komentosarjojen suorittamista tai ulkoisten työkalujen suorittamista, VCProj-tiedosto voi sisältää ohjeita näitä vaiheita varten.
- **Virheenkorjaus ja käyttöönotto:** VCProj-tiedosto voi sisältää virheenkorjaukseen, käyttöönottoon ja muihin projektikohtaisiin määrityksiin liittyviä asetuksia.

## Mikä on VCPROJ-tiedoston muoto?

VCProj-tiedostomuoto perustuu XML-kieleen (eXtensible Markup Language), joka on tavallinen strukturoidun datan esittelyn merkintäkieli. XML-muoto mahdollistaa projektikohtaisten tietojen ja asetusten organisoinnin ja tallentamisen hierarkkiseen rakenteeseen.

## Viitteet
* [Projekti- ja ratkaisutiedostot](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)


