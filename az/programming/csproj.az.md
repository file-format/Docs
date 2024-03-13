{
  "date": "2019-10-11",
  "keywords": [
"csproj faylı",
"csproj",
"uzadılması",
"format",
"csproj faylı nədir",
"csproj fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "CSPROJ faylları yarada və aça bilən CSPROJ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-azj"
}
},
  "lastmod": "2021-05-21"
}

## CSProj faylı nədir?
CSPROJ uzantısı olan fayllar sistem birləşmələrinə istinadlarla birlikdə layihəyə daxil edilmiş faylların siyahısını ehtiva edən C# layihə faylını təmsil edir. Microsoft VIiual Studio-da yeni layihə işə salındıqda, siz əsas həll ([.sln](/programming/sln/)) faylı ilə birlikdə bir .csproj faylı əldə edirsiniz. Əgər layihədə birdən çox məclis varsa, .sln faylının onları layihənin bir hissəsi kimi birləşdirdiyi yerdə bərabər sayda layihə faylı olacaq. Bu faylın məzmunu layihənin qurulması üçün tələb olunan bütün tələbləri müəyyən edir, məsələn, daxil ediləcək məzmun, platforma tələbləri, versiya məlumatları, veb server və ya verilənlər bazası serveri parametrləri və yerinə yetirilməli olan tapşırıqlar. Layihə faylının məzmunu XML fayl formatında yerləşdirilir və redaktə etmək, eləcə də baxmaq üçün istənilən mətn redaktorunda açıla bilər. O, həmçinin düzgün təşkili üçün layihə fayllarına məntiqi bir görünüş verir.

## CSPROJ Fayl Format #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Aşağıdakı bölmələr layihə faylı üçün fayl formatı elementlərini işləyib hazırlayır.

### Layihə Elementi ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) elementi hər bir layihə faylının kök elementidir. O, layihə faylı üçün XML sxemini müəyyən edir və qurma prosesi üçün giriş nöqtələrini təyin etmək üçün atributları daxil edə bilər.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Xüsusiyyətlər və Şərtlər

Xüsusiyyətlər layihənin qurulması üçün lazım olan məlumatları əks etdirir. Belə xassələr [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) elementi daxilində müəyyən edilir. Bu xassələr açar-dəyər cütlərindən ibarətdir ki, burada xassə elementinin adı xassə açarını, elementin məzmunu isə xassə dəyərini təyin edir. Məsələn, statik server adını və əlaqə sətirini saxlamaq üçün ServerName və ConnectionString adlı xassələri təyin edə bilərsiniz.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Elementi qiymətləndirmək üçün meyarları müəyyən etmək üçün şərtlər elementlər vasitəsilə müəyyən edilə bilər. Aşağıda göstərildiyi kimi əmlakı təyin edərkən bu, Şərt sözü ilə müəyyən edilir:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

MSBuild bu xassə tərifini emal edərkən, ilk olaraq **$(OutputRoot)** xassə dəyərinin mövcud olub olmadığını yoxlayır. Əmlak dəyəri boşdursa—başqa sözlə, istifadəçi bu xüsusiyyət üçün dəyər təqdim etməyibsə—şərt **true** olaraq qiymətləndirilir və əmlak dəyəri **..\Publish\Out.** olaraq təyin edilir.

### Elementlər və Element Qrupları

Layihə faylı, əslində fərqli fayl növləri olan qurma prosesinə girişləri müəyyən edir. MSBuild nomenklaturasında bu girişlər Element elementləri ilə təmsil olunur və [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) elementi daxilində müəyyən edilir. **Əmlak** elementləri kimi, siz də **Element** elementini istədiyiniz kimi adlandıra bilərsiniz. Bununla belə, elementin təmsil etdiyi faylı və ya joker simvolu müəyyən etmək üçün **Daxil et** atributunu göstərməlisiniz.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Hədəflər və Tapşırıqlar

[Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) elementi fərdi qurma təlimatını (və ya tapşırığını) təmsil edir. MSBuild çoxlu əvvəlcədən təyin edilmiş tapşırıqları ehtiva edir. Misal üçün:

* **Kopyala** tapşırığı faylları yeni yerə köçürür.

* **Csc** tapşırığı Visual C# kompilyatorunu işə salır.

* **Vbc** tapşırığı Visual Basic kompilyatorunu işə salır.

* **Exec** tapşırığı müəyyən edilmiş proqramı icra edir.

* **Mesaj** tapşırığı loggerə mesaj yazır.


Tapşırıqlar həmişə [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elementləri daxilində olmalıdır. **Hədəf** elementi ardıcıl olaraq yerinə yetirilən bir və ya bir neçə tapşırıq toplusudur və layihə faylında bir neçə hədəf ola bilər.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## İstinadlar

* [Layihə Faylını Anlamaq - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fayl)


