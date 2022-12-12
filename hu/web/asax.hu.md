{
  "date" : "2019-10-11",
  "keywords" :[ "asax", "asax fájl", "asax fájlformátum", "asax fájltípus", "fájl", "típus", "mi az asax fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET Server Application File",
  "description" :"Tanulja meg, mi az az ASAX fájl és API-k, amelyek ASAX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Mi az ASAX fájl?

Az .asax kiterjesztésű fájl az ASP.NET-alkalmazások által használt fájl, amely a szerver oldalon található. Kódot tartalmaz az ASP.NET vagy HTTP-modulok által keltett alkalmazás- és munkamenet-szintű eseményekre való reagáláshoz. Ez magában foglalja bizonyos események kezelését is, amikor az alkalmazás elindul vagy leáll. Az ASAX fájlok nem kötelezőek, és csak egyetlen ASAX fájl adható hozzá a webalkalmazásokhoz az alkalmazásszintű események és hibák globális szintű kezelésére. Az ASPX oldalakkal ellentétben az ASAX fájlok nem tartalmaznak kódot az alkalmazás funkcióinak megvalósításához.

## ASAX fájlformátum

Az ASAX fájlok egyszerű szöveges fájlformátumban vannak írva, és ember által olvashatóak. A leggyakrabban használt ASAX fájl a Global.asax, amely egy ASP.NET-alkalmazás gyökérkönyvtárában található. A webszerverek úgy vannak beállítva, hogy elutasítsák a fájlra érkező bejövő hívásokat, hogy megtiltsák a felhasználóknak a fájl kódjának letöltését vagy megtekintését.

### Global.ASAX – Példa az ASAX fájlformátumra

Egyetlen ASAX-fájl több szakaszból áll, amelyek az alkalmazásszintű események kezelésére vannak írva. Ezek a következők.

* **Alkalmazási direktívák** – Az alkalmazási direktívák olyan címkék, amelyek az ASP.NET elemző által a Global.asax fájl feldolgozásakor használandó opcionális alkalmazásspecifikus beállítások meghatározására szolgálnak. Ezek az utasítások a Global.asax fájl elején találhatók, és a következőképpen definiálhatók.

```
<%@ direktíva attribútum=érték [attribútum=érték … ]%>
```
* **Kóddeklarációs blokkok** - A kóddeklarációs blokkok a kiszolgálókód azon szakaszainak meghatározására szolgálnak, amelyek a \ fájlban található ASP.NET alkalmazásfájlokba vannak beágyazva.<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
* **Kódmegjelenítési blokkok** – Ezek határozzák meg az oldal renderelésekor végrehajtott soron belüli kódot vagy kifejezéseket. A kódmegjelenítési blokkok két stílusa a soron belüli kódot és a beágyazott kifejezéseket tartalmazza. Az előbbi az önálló kódsorok vagy blokkok meghatározására szolgál, míg az oldalsó parancsikonként a Write metódus hívására szolgál.

## Hivatkozások

* [HTTP-kezelők és HTTP-modulok áttekintése](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax szintaxis](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

