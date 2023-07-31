{
  "date" : "2020-01-11",
  "keywords" :[ "fișier x", "format fișier x", "ce este un fișier x", "fișier", "exemplu x", "extensie fișier x", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Format de fișier DirectX 2.0",
  "description":"Aflați despre formatul de fișier DirectX X și despre API-urile care pot deschide și crea fișiere DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Ce este un fișier X?

Un fișier cu extensia .x se referă la [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) Formatul de fișier vechi 3D Graphics care a fost introdus cu Microsoft DirectX 2.0. A fost folosit pentru redarea graficelor 3D în jocuri și specifică structurile pentru rețele, texturi, animații și obiecte definite de utilizator. A fost retras din 2014, deoarece formatul de fișier Autodesk FBX servește mai bine ca format mai modern. X este bazat pe șablon și nu are cunoștințe de utilizare.

Puteți deschide fișiere DirectX X folosind Microsoft DirectX și editoarele de text obișnuite.

## X Format de fișier

[Referința fișierului X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) conține informații de referință pentru elementele API care sunt utilizate pentru lucrați cu fișiere DirectX .x. Formatul oferă primitive de date de nivel scăzut care sunt utilizate de alte aplicații pentru a defini primitive de nivel superior prin șabloane de date. DirectX 6.0 a introdus interfețe și metode care permit citirea și scrierea în fișiere .x. DirectX 3.0 a introdus o versiune binară a acestui format de fișier.

[Referința formatului de fișier X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) definit de DirectX 9 conține informații de referință pentru .x fișiere în binar, precum și codificări text.

### Codificare binară

[Formatul binar](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definește formatul DirectX X ca o reprezentare tokenizată a formatului text. Aceste jetoane pot fi de sine stătătoare pentru a oferi structură gramaticală sau pot fi jetoane purtătoare de înregistrări care furnizează datele necesare.

#### Antet

Antetul binar poate fi citit și scris folosind următoarele definiții.

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

### Codificarea textului

Fișierele DirectX .x nu depind de modul în care este utilizat fișierul și nu sunt specifice nici unei aplicații. Această abordare bazată pe șablon permite ca formatul de fișier .x să fie utilizat de orice aplicație client.


#### Antet

Antetul cu lungime variabilă este obligatoriu și trebuie să fie la începutul fluxului de date. Antetul conține următoarele date.

|Tip |Sub tip |Dimensiune |Conținut |Sensul conținutului|
---|---|---|---|---|
|Număr magic (obligatoriu)| | 4 octeți |xof |
|Numărul versiunii (obligatoriu) |Numărul major |2 octeți |03 |Versiunea principală 3|
| |Număr minor |2 octeți |02 |Versiunea minoră 2|
|Tipul format (obligatoriu)| |4 octeți |"txt " |Fișier text|
| | | ||"bină"| Fișier binar|
| | | ||"tzip"| Fișier text comprimat MSZip|
| | | |"bzip"| Fișier binar comprimat MSZip|
|Dimensiunea plutitorului (obligatoriu)| |4 octeți| 0064| 64-bit floats|
| | | |0032 |32-bit floats|


## Referințe

* [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Referință pentru formatul fișierului DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

