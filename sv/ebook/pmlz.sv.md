{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Zipped Palm Markup Language File", "extension", "File", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om PMLZ-filformat, Palm Markup Language och API:er som kan skapa och öppna PMLZ-filer.",
  "title" :"PMLZ - Zipped Palm Markup Language File",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Vad är en PMLZ fil?

Palm Inc introducerade en eBook-filtyp; känt som PMLZ-filformatet som är en komprimerad version av [PML](/sv/ebook/pml/) filformat, det är därför filerna med .pmlz-tillägg kallas **Zipped Palm Markup Language File**. PMLZ-filen är bara en zip-behållare av en fil som kompilerar [PDB](/sv/ebook/pdb/)-filer för att skapa dokument för **eReader** (känd som en läsenhet för e-böcker som en surfplatta). PML-filen ger layouten till en PDB-fil (som innehåller olika datafiler) att visa på en Palm-enhet. Medan en PDB-fil är en databasfil som används av olika applikationer, inklusive Quicken, Pegasus, Microsoft Visual Studio och Palm Pilot. Kort sagt, en PMLZ är en komprimerad behållare med PML- och PDB-filer.


## Kunskap om Palm Markup Language
Följande tabell anger PML-kommandon:

|Kommando|Beskrivning|
---|---|
| \p | Ny sida |
| \x | Nytt kapitel; orsakar också en ny sidbrytning. Bifoga kapitelrubrik (och eventuella stilkoder) med \x och \x |
| \Xn | Nytt kapitel, indragna n nivåer (n mellan 0 och 4 inklusive) i kapiteldialogen; orsakar inte sidbrytning. Bifoga kapitelrubrik (och eventuella stilkoder) med \Xn och \Xn |
| \Cn="Kapiteltitel" | Infoga "Kapiteltitel" i kapitellistan, med nivå n (som \Xn). Texten visas inte på sidan och tvingar inte fram en sidbrytning. Detta kan ibland vara användbart för att t.ex. infoga ett kapitelmärke i början av en introduktion till kapitlet. |
| \c | Centrera detta textblock; stäng med \c på början av raden |
| \r | Högerjustera textblock; stäng med \r i början av raden |
| \i | Kursivera block; stäng med \i |
| \u | Stryk under block; stäng med \u |
| \o | Överslagsblock; stäng med \o |
| \v | Osynlig text; stäng med \v (kan användas för kommentarer) |
| \t | Indrag block. Börja i början av en rad, stäng med \t i slutet av en rad |
| \T="50%" | Dra in den angivna procentandelen av skärmens bredd, 50 % i detta fall. Om den aktuella ritpositionen redan är förbi den angivna skärmplatsen ignoreras denna tagg. |
| \w="50%" | Bädda in en horisontell regel för en given procentuell bredd på skärmen, i det här fallet 50 %. Den här taggen orsakar en radbrytning före och efter den. Regeln är centrerad. Procenttecknet är obligatoriskt. |
| \n | Byt till det "normala" typsnittet, som anges av användaren |
| \s | Byt till stdFont; stäng med \s för att återgå till normal font |
| \b | Byt till fetstil; stäng med \b för att återgå till normalt teckensnitt (utfasad; använd \B istället) |
| \l | Byt till largeFont; stäng med \l för att återgå till normal font |
| \B | Markera text som fetstil. Till skillnad från \b-taggen ändrar inte \B typsnittet, så du kan ha stor fet text. Du kan inte blanda \b och \B i samma PML-fil. |
| \Sp | Markera text som upphöjd. Bör inte blandas med andra stilar som fetstil, kursiv, etc. Bifoga upphöjd text med \Sp. |
| \Sb | Markera text som underskrift. Bör inte blandas med andra stilar som fetstil, kursiv, etc. Bifoga tecknad text med \Sb. |
| \k | Gör medföljande text till små bokstäver; sluta med \k. Alla tecken som är inneslutna i \k-taggar (inklusive de med accenter) görs med versaler och återges med en mindre punktstorlek än ett vanligt versaler. |
| \\ | Representerar ett enda snedstreck |
| \aXXX | Infoga icke-ASCII-tecken vars Windows-1252-kod är decimal XXX. Se PML-teckentabellen för detaljer. |
| \UXXXX | Infoga icke-ASCII-tecken vars Unicode-kod är hexadecimal XXXX. Se den utökade PML-teckentabellen för detaljer. |
| \m="imagename.png" | Infoga den namngivna bilden. Se avsnittet om bilder nedan. |
| \q="#linkanchor"En del text\q | Referera till ett länkankare som finns på en annan plats i dokumentet. Strängen efter ankarspecifikationen och före den avslutande \q är understruken eller visas på annat sätt vara en länk när dokumentet visas. |
| \Q="linkanchor" | Ange ett länkankare i dokumentet. |
| \- | Infoga ett mjukt bindestreck. Ett mjukt bindestreck visas bara om det är nödvändigt att bryta ett ord över en linje. |
| \Fn="fotnot1"1\Fn | Länka "1" till en fotnot vars namn är fotnot1, taggad i slutet av PML-dokumentet. Se avsnittet om fotnoter och sidofält nedan. |
| \Sd="sidebar1"Sidebar\Sd | Länka "Sidebar"-texten till ett sidofält vars namn är sidebar1, taggat i slutet av PML-dokumentet. Se avsnittet om fotnoter och sidofält nedan. |
| \I | Markera som ett referensindexobjekt. Bifoga indexobjekt (och eventuella stilkoder) med \I och \I.|


## Referenser

* [Palm Markup Language - By MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)

