{
  "date" : "2020-01-11",
  "keywords" :[ "soubor x", "formát souboru x", "co je soubor x", "soubor", "příklad x", "přípona souboru x", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Formát souboru DirectX 2.0",
  "description":"Další informace o formátu souborů DirectX X a rozhraních API, která mohou otevírat a vytvářet soubory DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Co je soubor X?

Soubor s příponou .x odkazuje na [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) starší formát souboru 3D grafiky, který byl zaveden s Microsoft DirectX 2.0. Byl použit pro vykreslování 3D grafiky ve hrách a specifikuje struktury pro sítě, textury, animace a uživatelem definované objekty. Od roku 2014 je zastaralý, protože formát souborů Autodesk FBX slouží lépe jako modernější formát. X je řízen šablonou a je bez jakýchkoliv znalostí o používání.

Soubory DirectX X můžete otevřít pomocí Microsoft DirectX a běžných textových editorů.

## Formát souboru X

[Odkaz na soubor X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) obsahuje referenční informace pro prvky API, které se používají k pracovat se soubory DirectX .x. Formát poskytuje datová primitiva nízké úrovně, která používají jiné aplikace k definování primitiv vyšší úrovně prostřednictvím datových šablon. DirectX 6.0 zavedlo rozhraní a metody, které umožňují čtení a zápis do souborů .x. DirectX 3.0 představil binární verzi tohoto formátu souboru.

[Odkaz na formát souboru X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) definovaný DirectX 9 obsahuje referenční informace pro .x soubory v binárním i textovém kódování.

### Binární kódování

[binární formát](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definuje formát DirectX X jako tokenizovanou reprezentaci textového formátu. Tyto tokeny mohou být samostatné, aby poskytovaly gramatickou strukturu, nebo to mohou být tokeny nesoucí záznamy, které poskytují potřebná data.

#### Záhlaví

Binární hlavičku lze číst a zapisovat pomocí následujících definic.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Kódování textu

Soubory DirectX .x nezávisí na způsobu použití souboru a nejsou specifické pro žádnou aplikaci. Tento přístup založený na šablonách umožňuje použití formátu souboru .x jakoukoli klientskou aplikací.


#### Záhlaví

Hlavička s proměnnou délkou je povinná a musí být na začátku datového toku. Záhlaví obsahuje následující údaje.

|Typ |Podtyp |Velikost |Obsah |Význam obsahu|
---|---|---|---|---|
|Magické číslo (povinné)| | 4 bajty |xof |
|Číslo verze (vyžadováno) |Hlavní číslo |2 bajty |03 |Hlavní verze 3|
| |Vedlejší číslo |2 bajty |02 |Vedlejší verze 2|
|Typ formátu (požadováno)| |4 bajty |"txt " |Textový soubor|
| | | |"přihrádka "| Binární soubor|
| | | |"zip"| Komprimovaný textový soubor MSZip|
| | | |"bzip"| MSZip komprimovaný binární soubor|
|Plováková velikost (požadováno)| |4 bajty| 0064| 64bitové plovoucí |
| | | |0032 |32bitové plováky|


## Reference

* [Soubory X Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Referenční informace o formátu souboru DirectX 9](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

