{
  "date": "2023-05-15",
  "keywords": [
"vcproj faylı",
"vcproj faylı nədir",
"vcproj faylının nümunəsi",
"vcproj faylında nə var",
"vcproj faylının formatı nədir",
"fayl",
"vcproj fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VCPROJ Fayl Format - Visual C++ Layihə Faylı",
  "description": "VCPROJ faylları yarada və aça bilən VCPROJ formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## VCPROJ faylı nədir?

A VCProj file, also known as Visual C++ Project file, is an XML-based file that stores configuration and settings for project in Microsoft Visual Studio. VCProj files are primarily used in older versions of Visual Studio, up to Visual Studio 2010. Visual Studio 2012-dən başlayaraq, layihə faylları VCXProj adlı yeni formata dəyişdirildi.

VCProj faylı layihənin mənbə kodu faylları, qurma parametrləri, kompilyator seçimləri, əlaqələndirici parametrləri və digər layihəyə xas konfiqurasiyalar haqqında məlumatları ehtiva edir. Layihənin necə qurulduğunu və hansı faylların layihəyə daxil edildiyini müəyyənləşdirir.

## VCPROJ faylının nümunəsi

VCProj faylının necə görünə biləcəyinə dair bir nümunə:

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

## VCPROJ faylında nə var?

VCProj faylı Microsoft Visual Studio-da Visual C++ layihəsi ilə bağlı müxtəlif elementləri və parametrləri ehtiva edir. VCProj faylında tapıla bilən bəzi əsas məlumatlar bunlardır:

- **Project Information:** The VCProj file includes project-level information such as the project name, project type, version, and unique identifier (GUID) for the projec-azt.
- **Platformalar və Konfiqurasiyalar:** O, layihə tərəfindən dəstəklənən platformaları və konfiqurasiyaları müəyyən edir. Platformalar Win32, x64 və ya ARM kimi hədəf platformanı müəyyən edir, konfiqurasiyalar isə Debug və ya Buraxılış kimi müxtəlif quruluş konfiqurasiyalarını müəyyənləşdirir.
- **Mənbə Faylları:** VCProj faylı C++ faylları, başlıq faylları, resurs faylları və digər əlaqəli fayllar daxil olmaqla, layihənin bir hissəsi olan mənbə kodu fayllarını siyahıya alır. Hər bir fayl adətən layihə qovluğuna nisbi yolu ilə müəyyən edilir.
- **Quraşdırma Parametrləri:** Buraya tərtibçi seçimləri, əlaqələndirici seçimlər, preprosessor tərifləri, əlavə daxiletmə kataloqları və əlavə asılılıqlar kimi qurma prosesi ilə bağlı parametrlər daxildir. Bu parametrlər layihənin necə qurulduğunu və əlaqələndirildiyini müəyyənləşdirir.
- **Öncədən tərtib edilmiş başlıqlar:** VCProj faylı layihənin əvvəlcədən tərtib edilmiş başlıqlardan istifadə edib-etmədiyini və əgər belədirsə, hansı faylın əvvəlcədən tərtib edilmiş başlıq kimi xidmət edəcəyini təyin edə bilər.
- **Çıxış Məlumatı:** O, icra olunan fayl, dinamik keçid kitabxanası (DLL) və ya statik kitabxana (LIB) kimi qurma prosesi tərəfindən yaradılan çıxış faylını və ya faylları müəyyən edir. Çıxış faylının yolu və adı VCProj faylında konfiqurasiya edilə bilər.
- **Referanslar:** VCProj faylında layihənin asılı olduğu digər layihələrə və ya xarici kitabxanalara istinadlar ola bilər. Bu istinadlar qurma prosesi zamanı asılılıqları həll etməyə kömək edir.
- **Xüsusi Quraşdırma Addımları:** Əgər layihə skriptləri işə salmaq və ya xarici alətləri icra etmək kimi əlavə fərdi qurma addımlarını tələb edirsə, VCProj faylına bu addımlar üçün təlimatlar daxil ola bilər.
- **Debugging and Deployment:** VCProj faylına sazlama, yerləşdirmə və digər layihəyə xas konfiqurasiyalarla bağlı parametrlər daxil ola bilər.

## VCPROJ faylının formatı nədir?

VCProj fayl formatı strukturlaşdırılmış məlumatların təqdim edilməsi üçün standart işarələmə dili olan XML-ə (genişləndirilə bilən işarələmə dili) əsaslanır. XML formatı iyerarxik strukturda layihəyə aid məlumat və parametrlərin təşkili və saxlanmasına imkan verir.

## İstinadlar
* [Layihə və Həll Faylları](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)


