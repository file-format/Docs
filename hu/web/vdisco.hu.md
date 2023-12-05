{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO File - DISCO Dynamic Discovery Document File Format",
  "description":"Ismerje meg, mi az a VDISCO fájl?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Mi az a VDISCO fájl?

A VDISCO fájl egy felfedezőfájl, amelyet a Microsoft Visual Studio használ a webszolgáltatásaiban. Információkat nyújt az elérhető webszolgáltatásokról, például URL-címeikről, névtereikről és metódusairól. A VDISCO fájl hasonló a [DISCO](/hu/web/disco/) fájlformátumhoz, de futás közben jön létre. A webszolgáltatás alkalmazásban tárolják, és a Visual Studio használja a webszolgáltatások dinamikus felfedezésére és használatára egy projektben. A VDISCO fájlok a tényleges Web Service kódot tartalmazó [.asmx](/hu/web/asmx/) fájllal együtt használatosak.

A VDISCO fájlt bármilyen szövegszerkesztőben megnyithatja, például a Microsoft Notepad, a Github Atom és az Apple TextEdit segítségével. Megnyitható a Microsoft Visual Studio 2012 és újabb verziójával is, hogy vele dolgozhasson.

## VDISCO fájlformátum

A VDISCO-fájlok mentése és tárolása [XML](/hu/web/xml/) fájlformátumban történik, amely egy univerzális formátum az adatok összeállításához és közzétételéhez. Tartalmazza a szolgáltatás URL-címét, névtereit és metódusait szabványos XML-címkékben, ahol minden címke a saját információinak megfelelő értékét tartalmazza.

## Hivatkozások

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# példa a DiscoveryClient osztályra](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

