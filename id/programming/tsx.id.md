{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File TSX - File React TypeScript - Apa itu file .tsx dan cara membukanya?",
  "description":"Pelajari tentang file TSX React TypeScript dan cara membukanya.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-id-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Apa itu berkas TSX?

Ekstensi file ".tsx" umumnya dikaitkan dengan file TypeScript yang berisi kode **React**. **TypeScript adalah superset JavaScript** yang menambahkan pengetikan statis ke bahasanya, dan **React adalah pustaka JavaScript untuk membangun antarmuka pengguna**. Saat bekerja dengan React dan TypeScript secara bersamaan, pengembang sering menggunakan ekstensi ".tsx" pada file mereka untuk menunjukkan bahwa file tersebut berisi TypeScript dan JSX (ekstensi sintaksis React untuk JavaScript).

## Contoh File TSX

TypeScript memungkinkan Anda menentukan tipe untuk variabel, parameter fungsi, dan lainnya. Anda akan sering melihat kode TypeScript dalam file ".tsx" yang menentukan jenis props, status, dan variabel lain yang digunakan dalam komponen React.

```
// Contoh: Kode TypeScript di komponen React
antarmuka MyComponentProps {
   nama: tali;
   usia: nomor;
}
const Komponen Saya: React.FC<MyComponentProps> = ({ nama, umur }) => {
   // Logika komponen di sini
   return <div>{name} berumur {age} tahun.</div>;
};
```

## JSX (Ekstensi Sintaks React)

JSX adalah ekstensi sintaksis untuk JavaScript yang direkomendasikan oleh React. Tampilannya mirip dengan XML/HTML dan digunakan untuk mendeskripsikan tampilan UI.

```
// Contoh: JSX dalam komponen React
const Komponen Saya: React.FC<MyComponentProps> = ({ nama, umur }) => {
   return <div>{name} berumur {age} tahun.</div>;
};
```

File ".tsx" biasanya berisi definisi komponen React yang menggunakan komponen fungsional atau komponen kelas.

```
// Contoh: React definisi komponen dalam file ".tsx".
const Komponen Saya: React.FC = () => {
   return <div>Halo, Bereaksi!</div>;
};
```

Anda akan sering melihat pernyataan import di awal file, yang membawa dependensi dan modul yang diperlukan.

```
// Contoh: Mengimpor pernyataan dalam file ".tsx".
impor Bereaksi dari 'bereaksi';
```

## Bagaimana cara membuka file TSX?

File TSX adalah file teks biasa sehingga Anda dapat membukanya di editor teks apa pun, misalnya. buku catatan. Namun, ini adalah file pengkodean dan dimaksudkan untuk dibuka oleh IDE misalnya. Kode Visual Studio.