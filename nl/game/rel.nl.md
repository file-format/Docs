{
  "date" : "2021-09-08",
  "keywords" :[ "rel file", "rel file format", "wat is een rel file", "file", "rel example", "rel file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over REL-bestandsindeling en API's die REL-bestanden kunnen maken en openen.",
  "title" :"REL - Verplaatsbaar modulebestand",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Wat is een REL-bestand?
Een bestand met de extensie .rel kan voor verschillende doeleinden worden gebruikt. Daarom staat het in termen van spelclassificatie bekend als een verplaatsbaar modulebestand dat wordt gebruikt door sommige Nintendo Wii-spellen, zoals Brawl, Super Smash Bros en Mario Kart Wii. Het omvat de gameplay-gegevens, inclusief personagemodellen en podia. REL-bestanden presteren op dezelfde manier als de .DLL-bestanden die door Microsoft Windows worden gebruikt.

## REL-bestandsindeling
In een REL-bestandsindeling is het bestand verdeeld in verschillende secties, gegroepeerd op soortgelijke toegang, bijv. alleen-lezen gegevens in één sectie, alle uitvoerbare code wordt in een andere geplaatst, enz. Het bestand begint met een koptekst, gevolgd door:
- Tabel met sectie-info.
- De sectiegegevens.
- Verhuisgegevens.

### Bestandskop
Het bestand begint met een header van maximaal 0x4C bytes:
| Verschuiving | Maat | Veldnaam | Beschrijving |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Willekeurig identificatienummer. Moet uniek zijn tussen alle REL's die door een game worden gebruikt. Mag niet 0 zijn. |
| 0x04 | 4 | volgende | Aanwijzer naar volgende module, gevuld tijdens runtime. |
| 0x08 | 4 | vorige | Pointer naar vorige module, gevuld tijdens runtime. |
| 0x0c | 4 | aantalSecties | Aantal secties in het bestand. |
| 0x10 | 4 | sectieInfoOffset | Offset naar het begin van de sectietabel. |
| 0x14 | 4 | naamOffset | Offset naar ASCII-tekenreeks die de naam van de module bevat. Kan NULL zijn. Ten opzichte van het begin van het REL-bestand. |
| 0x18 | 4 | naamGrootte | Grootte van de modulenaam in bytes. |
| 0x1c | 4 | versie | Versienummer van het REL-bestandsformaat. |
| 0x20 | 4 | bssMaat | Grootte van de sectie '.bss'. |
| 0x24 | 4 | relOffset | Offset naar de verhuistabel. |
| 0x28 | 4 | impOffset | Offset naar imp-tabel. |
| 0x2c | 4 | impSize | Grootte van imp-tabel in bytes. |
| 0x30 | 1 | prologSectie | Index in sectietabel met welke proloog relatief is. Overslaan als dit veld 0 is. |
| 0x31 | 1 | epilogSectie | Index in sectietabel waaraan epiloog relatief is. Overslaan als dit veld 0 is. |
| 0x32 | 1 | onopgeloste sectie | Index in sectietabel die onopgelost is ten opzichte van. Overslaan als dit veld 0 is. |
| 0x33 | 1 | bssSectie | Index in sectietabel waar bss relatief aan is. Gevuld tijdens runtime! |
| 0x34 | 4 | proloog | Offset in gespecificeerde sectie van de _prolog-functie. |
| 0x38 | 4 | epiloog | Offset naar gespecificeerde sectie van de _epilog-functie. |
| 0x3c | 4 | onopgelost | Offset naar gespecificeerde sectie van de _unresolved functie. |
| 0x40 | 4 | uitlijnen | Alleen versie ≥ 2. Uitlijningsbeperking voor alle secties, uitgedrukt als macht van 2. |
| 0x44 | 4 | bssUitlijnen | Alleen versie ≥ 2. Uitlijningsbeperking voor alle '.bss'-secties, uitgedrukt als macht van 2. |
| 0x48 | 4 | fixSize | Alleen versie ≥ 3. Als REL is gekoppeld aan OSLinkFixed (in plaats van OSLink), kan de spatie na dit adres voor andere doeleinden worden gebruikt (zoals BSS). |

### Sectie Info Tabel
De sectie-infotabel bevat **numSections**-items van elk 0x8 bytes lang:
| Verschuiving | Maat | Beschrijving |
-------|------------|-------------|
| 0x0 | 30 bits | Offset vanaf het begin van de REL naar de sectie. Als dit nul is, is de sectie een niet-geïnitialiseerde sectie (dwz .bss). |
| 0x3.6 | 1 beetje | Onbekend. |
| 0x3.7 | 1 beetje | Uitvoerbare vlag; als dit 1 is, is de sectie uitvoerbaar. |
| 0x4 | 4 | Lengte in bytes van de sectie. Als dit nul is, wordt deze invoer overgeslagen. |
| 0x8 | Volgende invoer | Volgende invoer |

### Verhuisgegevens
De verplaatsingsgegevens zijn een of meer lijsten van 0x8-bytestructuren. Het einde van elke lijst wordt gemarkeerd door de speciale typecode 203:
| Verschuiving | Naam | Maat | Beschrijving |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Offset in bytes van de vorige verhuizing naar deze. Als dit de eerste verplaatsing in de sectie is, is dit relatief ten opzichte van de sectiestart. |
| 0x2 | typ | 1 | Het verhuistype. Hieronder beschreven. |
| 0x3 | sectie | 1 | Het gedeelte van het symbool waartegen moet worden verplaatst. Voor het bijzondere verhuistype 202 is dit in plaats daarvan het nummer van de rubriek in dit bestand waarop de volgende verhuisvermeldingen van toepassing zijn. |
| 0x4 | toevoegen | 4 | Verschuiving in bytes van het symbool waartegen moet worden verplaatst, ten opzichte van het begin van zijn sectie. Dit is in plaats daarvan een absoluut adres voor verhuizingen tegen main.dol. |
| 0x8 | Volgende invoer | Volgende invoer | Volgende invoer |


 




## Referenties


* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


