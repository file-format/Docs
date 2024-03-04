{
  "date": "2020-01-11",
  "keywords": [
"x failą",
"x failo formatas",
"kas yra x failas",
"failą",
"x pavyzdys",
"x failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X – „DirectX 2.0“ failo formatas",
  "description": "Sužinokite apie „DirectX X“ failų formatą ir API, kurios gali atidaryti ir kurti „DirectX X“ failus.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--ltx"
}
},
  "lastmod": "2020-01-11"
}

## Kas yra X failas?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. Jis buvo naudojamas 3D grafikos atvaizdavimui žaidimuose ir nurodo tinklelių, tekstūrų, animacijų ir vartotojo apibrėžtų objektų struktūras. Jis nebenaudojamas nuo 2014 m., nes Autodesk FBX failo formatas geriau tinka kaip modernesnis formatas. X yra pagrįsta šablonu ir neturi jokių naudojimo žinių.

DirectX X failus galite atidaryti naudodami Microsoft DirectX ir įprastas teksto rengykles.

## X failo formatas

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) yra nuorodos informacija apie API elementus, kurie naudojami dirbti su DirectX .x failais. Formatas suteikia žemo lygio duomenų primityvus, kuriuos kitos programos naudoja aukštesnio lygio primityvams apibrėžti per duomenų šablonus. DirectX 6.0 pristatė sąsajas ir metodus, leidžiančius skaityti ir rašyti iš .x failų. DirectX 3.0 pristatė dvejetainę šio failo formato versiją.

DirectX 9 apibrėžtoje [X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) yra nuorodos informacija apie .x failus dvejetainiuose ir teksto kodavimuose.

### Dvejetainis kodavimas

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) apibrėžia DirectX X formatą kaip tokenizuotą teksto formato atvaizdą. Šie žetonai gali būti atskiri, kad suteiktų gramatinę struktūrą, arba gali būti įrašą turintys žetonai, teikiantys reikiamus duomenis.

#### Antraštė

Dvejetainę antraštę galima skaityti ir rašyti naudojant šiuos apibrėžimus.

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

### Teksto kodavimas

DirectX .x failai nepriklauso nuo to, kaip failas naudojamas, ir nėra būdingi jokiai programai. Šis šablonu pagrįstas metodas leidžia .x failo formatą naudoti bet kuriai kliento programai.


#### Antraštė

Kintamo ilgio antraštė yra privaloma ir turi būti duomenų srauto pradžioje. Antraštėje yra šie duomenys.

|Tipas |Potipis |Dydis |Turinys |Turinio reikšmė|
---|---|---|---|---|
|Magiškasis numeris (būtinas)| | 4 baitai |xof |
|Versijos numeris (būtinas) |Pagrindinis numeris |2 baitai |03 |Pagrindinė versija 3|
| |Nedidelis skaičius |2 baitai |02 |Mažoji versija 2|
|Formato tipas (būtinas)| |4 baitai |txt |Teksto failas|
| | | |bin | Dvejetainis failas|
| | | |tzip| MSZip suspausto teksto failas|
| | | |bzip| MSZip suspaustas dvejetainis failas|
|Plūdės dydis (būtinas)| |4 baitai| 0064| 64 bitų plūdės|
| | | |0032 |32 bitų plaukiojantieji|


## Nuorodos

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 failo formato nuoroda](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

