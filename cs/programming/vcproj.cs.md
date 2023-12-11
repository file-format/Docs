{
"datum": "2023-05-15",
  "keywords": [
"soubor vcproj",
"co je soubor vcproj",
"příklad souboru vcproj",
"co obsahuje soubor vcproj",
"jaký je formát souboru vcproj",
"soubor",
"přípona souboru vcproj",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru VCPROJ - soubor projektu Visual C++",
  "description":"Další informace o formátu VCPROJ a rozhraních API, která mohou vytvářet a otevírat soubory VCPROJ.",
  "linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Co je soubor VCPROJ?

Soubor VCProj, také známý jako soubor projektu Visual C++, je soubor založený na XML, který ukládá konfiguraci a nastavení pro projekt v Microsoft Visual Studio. Soubory VCProj se primárně používají ve starších verzích sady Visual Studio až po Visual Studio 2010. Počínaje Visual Studiem 2012 byly soubory projektu změněny na nový formát s názvem VCXProj.

Soubor VCProj obsahuje informace o souborech zdrojového kódu projektu, nastavení sestavení, možnostech kompilátoru, nastavení linkeru a dalších konfiguracích specifických pro projekt. Definuje, jak je projekt sestaven a jaké soubory jsou v projektu zahrnuty.

## Příklad souboru VCPROJ

Zde je příklad toho, jak může soubor VCProj vypadat:

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

## Co obsahuje soubor VCPROJ?

Soubor VCProj obsahuje různé prvky a nastavení související s projektem Visual C++ v Microsoft Visual Studio. Zde jsou některé klíčové informace, které lze nalézt v souboru VCProj:

- **Informace o projektu:** Soubor VCProj obsahuje informace na úrovni projektu, jako je název projektu, typ projektu, verze a jedinečný identifikátor (GUID) projektu.
- **Platformy a konfigurace:** Specifikuje platformy a konfigurace podporované projektem. Platformy definují cílovou platformu, jako je Win32, x64 nebo ARM, zatímco konfigurace definují různé konfigurace sestavení, jako je Debug nebo Release.
- **Zdrojové soubory:** Soubor VCProj uvádí soubory zdrojového kódu, které jsou součástí projektu, včetně souborů C++, hlavičkových souborů, zdrojových souborů a dalších souvisejících souborů. Každý soubor je obvykle specifikován svou relativní cestou k adresáři projektu.
- **Nastavení sestavení:** Zahrnuje nastavení související s procesem sestavení, jako jsou možnosti kompilátoru, možnosti linkeru, definice preprocesoru, další adresáře zahrnutí a další závislosti. Tato nastavení definují, jak je projekt sestaven a propojen.
- **Předkompilovaná záhlaví:** Soubor VCProj může určit, zda projekt používá předkompilovaná záhlaví, a pokud ano, který soubor slouží jako předkompilované záhlaví.
- **Informace o výstupu:** Definuje výstupní soubor nebo soubory generované procesem sestavení, jako je spustitelný soubor, dynamická knihovna (DLL) nebo statická knihovna (LIB). Cesta a název výstupního souboru lze nakonfigurovat v souboru VCProj.
- **Odkazy:** Soubor VCProj může obsahovat odkazy na jiné projekty nebo externí knihovny, na kterých projekt závisí. Tyto odkazy pomáhají vyřešit závislosti během procesu sestavení.
- **Kroky vlastního sestavení:** Pokud projekt vyžaduje další kroky vlastního sestavení, jako je spouštění skriptů nebo spouštění externích nástrojů, soubor VCProj může obsahovat pokyny pro tyto kroky.
- **Ladění a nasazení:** Soubor VCProj může obsahovat nastavení související s laděním, nasazením a dalšími konfiguracemi specifickými pro projekt.

## Jaký je formát souboru VCPROJ?

Formát souboru VCProj je založen na XML (eXtensible Markup Language), což je standardní značkovací jazyk pro reprezentaci strukturovaných dat. Formát XML umožňuje organizaci a ukládání informací a nastavení specifických pro projekt v hierarchické struktuře.

## Reference
* [Soubory projektů a řešení](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)

