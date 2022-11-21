{
  "date" : "2021-10-20",
  "keywords" :[ "file bns", "format file bns", "apa itu file bns", "file", "contoh bns", "ekstensi file Skrip Peta Bonus Portal", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file BNS Skrip Peta Bonus ortal dan API yang dapat membuat dan membuka file BNS.",
  "title" :"BNS - File Skrip Peta Bonus Portal",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Apa itu file BNS?

File dengan ekstensi .bns adalah file skrip game yang dibuat dengan game pemecahan teka-teki Portal Map yang dikembangkan oleh Valve. Ini berisi skrip teks untuk menentukan informasi tentang peta Portal yang disimpan sebagai file .bsp. File BNS digunakan sebagai referensi untuk file peta aktual ini dan berisi daftar tantangan yang harus diselesaikan. Selain itu, berisi nama peta, komentar tentang peta, dan referensi file gambar thumbnail. File BNS dapat dibuka di editor teks apa pun seperti Notepad ++, textEdit, dan Notepad.

## Format File BNS

File BNS disimpan sebagai file teks biasa yang dapat dibaca manusia. Ini dapat dibuka di editor teks dan diedit juga. Namun, ini harus diedit dengan hati-hati untuk menghindari kesalahan dalam skrip.

## Contoh Format File BNS

File BNS mungkin terlihat seperti berikut saat dibuka di editor teks seperti Notepad++.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## Bagian dari File BNS

Dalam contoh di atas,

* `#Bonus_Map_Challenges` - Mewakili nama peta.
* `peta` - Mewakili nama peta yang akan dimasukkan ke dalam folder peta game
* `bab` - Mewakili bab yang dimiliki peta. Semua file bab terletak di file VPK dengan menambahkan nama peta dalam format `map your_map_name`
* `Gambar` - Ini berisi thumbnail peta dan disimpan di jalur root steam\steamapps\common\portal\portal\materials\VGUI.
* `Komentar` - Teks deskriptif tentang peta yang dibuat.

## Referensi

* [Skrip Tantangan Portal](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

