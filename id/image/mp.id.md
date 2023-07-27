{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Berkas MP - Berkas MetaPost LaTeX",
  "description":"Pelajari tentang format file MP dan API yang dapat membuat dan membuka file MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Apa itu file MP?

File MP adalah file gambar vektor yang dihasilkan oleh bahasa pemrograman MetaPost untuk membuat gambar. Gambar vektor yang dibuat menggunakan format file MP disimpan sebagai file [EPS](/id/page-description-language/eps/) (Encapsulated PostScript). Selain itu, MetaPost didistribusikan dengan kerangka TeX dan Metafont dan file MP dapat dibuat dari dalam file TEX dan LTX yang digunakan oleh aplikasi ini. File MP berisi pernyataan gambar dan gambar algoritmik matematika untuk merender file EPS keluaran. Mesin PDFTex dapat menggunakan EPS yang dibuat untuk menghasilkan file [PDF](/id/pdf/) secara langsung.

## Format File MP

File MP disimpan ke disk sebagai file biner dan menghasilkan keluaran EPS saat diekspor ke format file gambar vektor keluaran. Gambar yang dibuat menggunakan MetaPost disertakan dalam bentuk yang diformat di dalam dokumen teknis dan publikasi jurnal yang dibuat dengan LaTex.

### Contoh Berkas MP MetaPost

Berikut adalah contoh, dirujuk dari [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), yang berisi panah dan huruf "A" tepat di atas tengah anak panah.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referensi ##

* [MetaPost oleh Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Sampel Metapost lateks oleh Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

