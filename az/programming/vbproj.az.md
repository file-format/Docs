{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"fayl",
"uzadılması",
"fayl formatı",
"VB Layihə Faylı",
"Proqramlaşdırma bələdçisi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "VBPROJ faylları yarada və aça bilən VBPROJ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-azj"
}
},
  "lastmod": "2020-09-10"
}

## VBPROJ faylı nədir?

.vbproj uzantısı olan fayl Microsoft-un MSBuild mühərriki tərəfindən layihələri Visual Studio həlli çərçivəsində qurmaq üçün istifadə edilən Microsoft Visual Basic layihə faylıdır. O, [C#](/programming/cs/) dilində yazılmış .NET layihələri üçün [CSPROJ](/programming/csproj/) faylına bənzəyir. MSBuild mühərriki VBPROJ fayllarından müxtəlif qruplarda olan məlumatları oxuyur və çıxış faylını yaradır. VBPROJ faylı layihəni təyin edən qlobal identifikatorlar, siniflər və xassələrlə bağlı məlumatları ehtiva edə bilər. VBPROJ faylları Microsoft Visual Studio və Windows və MacOS Əməliyyat Sistemlərində Notepad kimi hər hansı ümumi mətn redaktoru ilə açıla və redaktə edilə bilər.

## VBPROJ Fayl Format - Ətraflı Məlumat

VBPROJ faylları [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019) əsasında [XML](/web/xml/) fayl formatında yazılmış mətn fayllarıdır. VBPROJ faylı həmin xüsusi parametrlər qrupu ilə əlaqəli məlumatları müəyyən edən XML teqləri şəklində məlumat ehtiva edir. Bu parametr fayllarını Microsoft Visual Studio IDE-də açmaq və redaktə etmək çox tövsiyə olunur.

### VBPROJ Elementləri

VB Parametrlər faylının tərkib elementləri aşağıdakı şəkildə göstərildiyi kimidir.

{{< figure src="../vbproj.png" alt="VBPROJ fayl formatı" >}}

The following table gives a brief description of these elements.

|Element|Təsvir|
---|---|
|Layihə| Hər bir layihə faylının kök elementidir və layihə faylı üçün XML sxeminin müəyyən edilməsinə əlavə olaraq tikinti prosesi üçün giriş nöqtələrini müəyyən etmək üçün atributları ehtiva edə bilər|
|Xassələr və Şərtlər| Xüsusiyyətlər Açar-dəyər cütlərindən ibarətdir və PropertyGroup elementi ilə müəyyən edilir. Əmlak elementinin adı xassə açarını təmsil edir və elementin məzmunu xassə dəyərini müəyyən edir.|
|Elementlər və Maddə Qrupları|Layihə faylındakı elementlər tikinti prosesinin bir hissəsi kimi tələb olunan fayl-kod faylları, konfiqurasiya faylları, əmr faylları və digərləri kimi tikinti prosesinə daxil olan məlumatlardır. Elementlər ItemGroup elementi daxilindədir və müəyyən edilməlidir.|
|Hədəflər və Tapşırıqlar| Tapşırıq elementi fərdi qurma təlimatını (və ya tapşırığını) təmsil edir. MSBuild-ə Copy, CSC, VBC, Exec kimi çoxlu əvvəlcədən təyin edilmiş tapşırıqlar daxildir. Tapşırıqlar həmişə ardıcıl olaraq yerinə yetirilən bir və ya bir neçə tapşırıq dəsti olan Hədəf Elementində olmalıdır və layihə faylında bir neçə hədəf ola bilər.|

## İstinadlar

* [Layihə Faylını Anlamaq](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


