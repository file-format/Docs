{
  "date": "2019-10-11",
  "keywords": [
"asax",
"asax faylı",
"asax fayl formatı",
"asax fayl növü",
"fayl",
"növü",
"asax faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX - ASP.NET Server Tətbiq Faylı",
  "description": "ASAX faylının nə olduğunu və ASAX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-azx"
}
},
  "lastmod": "2021-06-07"
}

## ASAX faylı nədir?

.asax uzantısı olan fayl server tərəfində yerləşən ASP.NET proqramları tərəfindən istifadə edilən fayldır. O, ASP.NET və ya HTTP modulları tərəfindən qaldırılan proqram səviyyəli və sessiya səviyyəli hadisələrə cavab vermək üçün kod ehtiva edir. Buraya həmçinin proqram işə salındıqda və ya bağlandıqda müəyyən hadisələrin idarə edilməsi daxildir. ASAX faylları isteğe bağlıdır və qlobal səviyyədə tətbiq səviyyəli hadisələri və səhvləri idarə etmək üçün veb proqramlara yalnız bir ASAX faylı əlavə olunur. ASPX səhifələrindən fərqli olaraq, ASAX fayllarında tətbiqin funksionallığını həyata keçirmək üçün heç bir kod yoxdur.

## ASAX fayl formatı

ASAX faylları düz mətn faylı formatında yazılır və insanlar tərəfindən oxuna bilər. Ən çox istifadə edilən ASAX faylı ASP.NET tətbiqinin kök kataloqunda yerləşən Global.asax faylıdır. Veb Serverlər istifadəçilərə bu faylın kodunu yükləməyi və ya baxmağı qadağan etmək üçün bu fayla daxil olan hər hansı zəngləri rədd etmək üçün konfiqurasiya edilmişdir.

### Global.ASAX - ASAX Fayl Formatının Nümunəsi

Tək ASAX faylı proqram səviyyəsində hadisələri idarə etmək üçün yazılmış bir neçə bölmədən ibarətdir. Bunlar aşağıdakı kimidir.

 * **Tətbiq Direktivləri** - Tətbiq direktivləri Global.asax faylını emal edərkən ASP.NET analizatoru tərəfindən istifadə ediləcək əlavə proqrama aid parametrləri müəyyən etmək üçün istifadə olunan teqlərdir. Bu direktivlər Global.asax faylının başlanğıcında yerləşir və aşağıdakı kimi müəyyən edilir.

```
<%@ direktiv atribut=dəyər [atribut=dəyər … ]%>
```
 * **Kod Bəyannaməsi Blokları** - Kod bəyannamə blokları ASP.NET proqram fayllarına daxil edilmiş server kodunun bölmələrini müəyyən etmək üçün istifadə olunur.<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
 * **Kod İşlətmə Blokları** - Bunlar səhifənin göstərildiyi zaman yerinə yetirilən daxili kodu və ya ifadələri müəyyən edir. Kod göstərmə bloklarının iki üslubuna daxili kod və daxili ifadələr daxildir. Birincisi öz-özünə daxil olan xətləri və ya kod bloklarını təyin etmək üçün istifadə olunur, yanal isə Write metodunu çağırmaq üçün qısa yol kimi istifadə olunur.

## İstinadlar

 * [HTTP İşləyiciləri və HTTP Modullarına Baxış](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Sintaksisi](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

