{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aflați despre formatul de fișier MDS și despre API-urile care pot crea și deschide fișiere MDS.",
  "title" : "Format Fișier MDS - Fișier Sidecar Descriptor Media",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-ro",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Ce este un fișier MDS?

MDS (Media Descriptor Sidecar File) este un fișier asociat cu software-ul Alcohol 120% și Daemon Tools, ambele fiind utilizate pentru crearea și gestionarea unităților CD și DVD virtuale. Fișierul MDS conține informații despre aspectul datelor de pe disc, inclusiv locația tuturor fișierelor și structura discului. Acest lucru permite unității virtuale să emuleze comportamentul unui disc fizic, astfel încât software-ul să poată citi datele de pe discul virtual ca și cum ar fi un disc real.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## Relația cu alcoolul 120%

Alcohol 120% este un software popular pentru crearea și gestionarea unităților CD și DVD virtuale și utilizează formatul de fișier MDS pentru a salva și a accesa imaginile de disc. Formatul de fișier MDS este proprietarul Alcohol 120% și poate fi deschis și utilizat numai de software-ul Alcohol 120% sau de alt software care îl acceptă.

## Cum se deschide fișierul MDS?

Pentru a deschide un fișier MDS în Alcohol 120%, ar trebui să aveți software-ul instalat pe computer. După ce ați instalat Alcohol 120%, puteți deschide fișierul MDS făcând următoarele:

1. Lansați Alcool 120%.
2. Faceți clic pe meniul Fișier” și selectați Deschidere”.
3. Navigați la locația fișierului MDS pe computer și selectați-l.
4. Fișierul MDS va fi deschis acum în Alcool 120% și vi se va solicita să selectați fișierul imagine corespunzător (cum ar fi ISO, BIN sau CUE).
5. După ce selectați fișierul imagine, Alcohol 120% va monta imaginea pe o unitate virtuală.

Alternativ, puteți deschide și un fișier MDS făcând dublu clic pe el, dacă Alcohol 120% este setat ca program implicit pentru deschiderea fișierelor MDS. De asemenea, puteți utiliza alte software care acceptă formatul MDS, cum ar fi Daemon Tools, Virtual CloneDrive, Virtual Drive Manager și MagicISO.

## Referințe
* [Alcool 120% - software de inscripționare CD și DVD](https://www.alcohol-soft.com/)


