{
  "date": "2021-06-29",
  "keywords": [
"com failu",
"kas ir com fails",
"failu",
"com piemērs",
"com faila paplašinājumu",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par COM faila formātu un API, kas var izveidot un atvērt COM failus.",
  "title": "COM — DOS komandas faila formāts",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-lvm"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir COM fails?
COM faili tiek vienkārši izmantoti, lai izpildītu komandu vai instrukciju kopu. COM fails sastāv no izpildāmas programmas, kuru var palaist no Windows vai MS-DOS. Tāpat kā EXE fails, arī COM fails tiek saglabāts binārā formātā, taču tas atšķiras no EXE faila, jo tam nav galvenes vai metadatu, kā arī tā maksimālais izmērs ir aptuveni 64 KB. Kad COM fails pirmo reizi palaižas 32 bitu sistēmā, tas aicina instalēt NT virtuālās DOS mašīnas (NTVDM) komponentu. COM failu var palaist Microsoft Windows 64 bitu versijā ar virtuālo mašīnu, kas atbalsta MS-DOS vidi.

## COM faila formāts
COM faila formāts ir binārs izpildāms formāts, ko izmanto operētājsistēmā Microsoft Windows vai MS-DOS. Tās struktūra sastāv tikai no instrukciju kopas; tai nav galvenes un standarta metadatu. Tas glabā visus savus datus un kodu tikai vienā segmentā, un tā binārais faila lielums nepārsniedz 64 KB. Šis faila formāts nepārvietojas, mēģinot palaist atkārtoti. Tātad operētājsistēma to ielādē iepriekš iestatītā adresē. Turklāt ir iespējams izveidot COM failu, kas tiek izpildīts abās operētājsistēmās **fat bināra** formā. Instrukciju līmenī nav faktiskas saderības. Instrukcijas ievades punktā ir atlasītas tā, lai tās būtu vienādas funkcionalitātē, bet atšķirīgas abās operētājsistēmās, un liek programmai darboties, pāriet uz izmantotās operētājsistēmas sadaļu. Būtībā tās ir divas dažādas programmas ar vienu un to pašu procedūru vienā failā, pirms kuras tiek izvēlēts izmantojamais kods.
### COM faila piemērs
Palaižot COM failu, instrukcijas tiek nolasītas no pirmā baita un tiek izpildītas secīgi, līdz tiek atrastas pēdējās instrukcijas. Šeit ir ASM koda piemērs:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Atsauces 

* [COM fails — Wikipewdia](https://en.wikipedia.org/wiki/COM_file)


