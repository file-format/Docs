{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME fájl – Mi az a .time fájl? A fájl létrehozásának ideje Linux alatt",
  "description" : "Ismerje meg a TIME fájlt, és ismerje meg a fájl létrehozásának idejét Linux alatt",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-hu",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mi az a TIME fájl?

A TIME fájlformátumot a LIGHT nevű webrendszer használta, amely segített a felhasználóknak életük rögzítésében, rendszerezésében és megosztásában. Lényegében bejegyzések gyűjteményét tárolta, és egy mappát képviselt a rendszeren belül a felhasználó életoldalán.

## Hogyan lehet megtudni, mikor jött létre egy fájl Linux alatt

Linux alatt a `stat` paranccsal megtudhatja, mikor jött létre a fájl. A következőképpen teheti meg:

Nyisson meg egy terminált, és írja be a következő parancsot:

```
stat <file_path>
```

Cserélje ki a `<file_path> ` az Önt érdeklő fájl elérési útjával. Például:

```
stat /path/to/your/file.txt
```

Ez a parancs különféle információkat jelenít meg a fájlról, beleértve a létrehozási idejét is. Keresse meg a Születés” vagy Fájl:” karakterlánccal kezdődő sort. A Születési” idő azt jelzi, hogy a fájl mikor jött létre a fájlrendszeren.

Íme egy példa, hogyan nézhet ki a kimenet:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Ebben a példában a Születési” idő a fájl létrehozásának időpontját jelzi.

