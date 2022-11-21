{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "file", "ekstensi", "format file", "Bahasa prоgrаmming NUT", "Panduan Pemrograman", "Contoh NUT", "format file NUT", "bahasa tupai", "file ekstensi .nut ", "file NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Berkas Bahasa Tupai",
  "description":"Pelajari tentang format file NUT dan API yang dapat membuat dan membuka file NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Apa itu file NUT?

NUT mengacu pada file NUT Open Container Format. Format file NUT ini milik bahasa pemrograman yang dikenal sebagai Squirrel. Ini adalah bahasa pemrograman berorientasi objek, tingkat tinggi dan imperatif yang sebagian besar digunakan dalam sistem tertanam dan video game.

Bahasa tupai dianggap sebagai bahasa skrip ringan yang dapat dengan mudah disesuaikan menurut ukuran dan lebar pita. Ini melibatkan keuntungan penghitungan referensi otomatis dan pengelolaan sampah di memori.

Sintaks bahasa tupai menarik para pengembang karena mirip dengan C dan melibatkan fitur bahasa scripting. Tapi tetap saja, ini memiliki keuntungan yang lebih sedikit dibandingkan dengan bahasa pemrograman lain yang lebih populer untuk tujuan ini.



## Sejarah Singkat ##

Ini dirancang oleh Alberto Demichelis pada tahun 2003. Namun, versi stabil dari bahasa ini dirilis pada tahun 2016. Ini dirancang di bawah lisensi zlib/libpng. Pada tahun 2010 lisensi diubah dan dialihkan ke MIT. Bahasa ini dianggap sebagai versi terinspirasi dari [LUA](/id/programming/lua/) (Bahasa pemrograman). Ada daftar saran untuk bahasa sebelumnya di situs web yang dirancang oleh Alberto agar lebih menguntungkan.


## Spesifikasi teknis ##

Fitur dan spesifikasi bahasa tupai beragam. Ini menyediakan fasilitas pengetikan Dinamis, properti delegasi, beberapa penggunaan kelas dan antarmuka. Sintaks bahasa ini memiliki kemiripan dengan sintaks bahasa C. Aplikasi seperti Enduro/X (server aplikasi cluster) menggunakan bahasa ini. Karena Squirrel juga digunakan untuk video game, beberapa di antaranya adalah OpenTTD, GTA IV, dll.

Rilis bahasa yang stabil adalah 3.0.7. Toolkit yang dikenal sebagai MirthKit menggunakan bahasa pemrograman Squirrel untuk menyediakan open-source dan cross-platform untuk game dua dimensi. Sifat bahasa ini dinamis dan sebagian besar fiturnya mirip dengan [Python](/id/programming/py/), LUA, dll. Ini juga melibatkan penerapan VM berbasis register. Kinerja Squirrel lebih lambat dibandingkan dengan LUA.

Ada juga jenis file ekstensi ".nut" lainnya, itulah sebabnya Anda harus melihat ukuran file untuk mengetahui file NUT mana yang Anda miliki. File NUT skrip tupai sebagian besar lebih kecil dari 1 MB sedangkan file NUT video biasanya lebih besar dari 1 MB.


## Contoh Format File NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Referensi ##

* [NUT - oleh Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



