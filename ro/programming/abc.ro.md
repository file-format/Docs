
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - Fișier de cod de octet ActionScript",
  "description":"Aflați despre ce este formatul de fișier ABC cu exemple și API-uri care pot crea și deschide fișiere ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Ce este un fișier ABC?

Un fișier cu extensia .abc este un fișier ActionScript Byte Code creat de compilatorul Flash ca rezultat al compilării fișierelor script ActionScript. Codul octet conținut în fișierul ABC este executat de mașina virtuală ActionScript (AVM și AVM2). Codul octet cuprinde date constante, instrucțiuni din setul de instrucțiuni AVM2 și diferite tipuri de metadate. Când un fișier ABC este încărcat în AVM sau AVM2, acesta este supus verificării. Dacă nu este conform cu Prezentare generală AVM2, este respins. Fișierele ABC pot fi deschise în Adobe Flash Player, care a fost întrerupt cu mult timp în urmă.

## Format de fișier ABC - Mai multe informații

Fișierele ABC sunt salvate pe disc în format de fișier binar care pot fi citite de mașinile virtuale AVM sau AVM2. Structura sa internă de fișiere reprezintă blocul de cod executabil cu toate datele sale constante, descriptorii de tip, codul și metadatele.

## Structura fișierului ABC

Structura fișierului ABC este așa cum se arată mai jos.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Câmpurile fișierului ABC

|Nume câmp|Descriere|
---|---|
|versiune_minor, versiune_major|Valorile versiunii_major și versiunii_minore sunt numerele versiunii majore și minore ale formatului abcFile.|
|constant_pool|Constanta_pool este o structură de lungime variabilă compusă din numere întregi, duble, șiruri, spații de nume, seturi de spații de nume și nume multiple.|
|method_count, method|Valoarea ofmethod_count este numărul de intrări din matricea metodei. Fiecare intrare din tabloul de metode este o structură de lungime variabilă method_info.|
|metadata_count, metadata|Valoarea metadata_count este numărul de intrări din matricea de metadate. Fiecare intrare de metadate este o metadata_infostructure care mapează un nume la un set de valori șir. |
|class_count, instance, class|Valoarea class_count este numărul de intrări din matricele de instanță și de clasă. |
|script_count, script|Valoarea script_count este numărul de intrări din matricea de script. Fiecare intrare de script este o structură script_info care definește caracteristicile unui singur script din acest fișier. |
|method_body_count, method_body|Valoarea method_body_count este numărul de intrări din tabloul method_body. Fiecare method_bodyentry constă dintr-o structură de lungime variabilă method_body_info care conține instrucțiuni pentru o metodă sau funcție individuală.|

## Referințe

* [ABC robust (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

