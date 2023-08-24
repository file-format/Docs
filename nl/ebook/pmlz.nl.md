{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Zipped Palm Markup Language File", "extensie", "File", "format", "eBook", "Palm Markup Language"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over PMLZ-bestandsindeling, Palm Markup Language en API's die PMLZ-bestanden kunnen maken en openen.",
  "title" :"PMLZ - gezipt Palm Markup Language-bestand",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Wat is een PMLZ-bestand?

Palm Inc introduceerde een eBook-bestandstype; bekend als het PMLZ-bestandsformaat, een gecomprimeerde versie van het [PML](/nl/ebook/pml/)-bestandsformaat. Daarom staan de bestanden met de extensie .pmlz bekend als **Zipped Palm Markup Language File**. Het PMLZ-bestand is slechts een zip-container van een bestand dat [PDB](/nl/programming/pdb/)-bestanden compileert om documenten te maken voor **eReader** (bekend als een apparaat voor het lezen van e-boeken, zoals een tabletcomputer). Het PML-bestand geeft de lay-out aan een PDB-bestand (met verschillende gegevensbestanden) om op een Palm Device weer te geven. Terwijl een PDB-bestand een databasebestand is dat door verschillende toepassingen wordt gebruikt, waaronder Quicken, Pegasus, Microsoft Visual Studio en Palm Pilot. Kortom, een PMLZ is een gecomprimeerde container met PML- en PDB-bestanden.


## Kennis over Palm Markup Language
De volgende tabel specificeert de PML-opdrachten:

|Commando|Beschrijving|
---|---|
| \p | Nieuwe pagina |
| \x | Nieuw hoofdstuk; veroorzaakt ook een nieuw pagina-einde. Sluit hoofdstuktitel (en eventuele stijlcodes) in met \x en \x |
| \Xn | Nieuw hoofdstuk, n niveaus ingesprongen (n tussen 0 en 4 inclusief) in het dialoogvenster Hoofdstuk; veroorzaakt geen pagina-einde. Voeg hoofdstuktitel (en eventuele stijlcodes) toe met \Xn en \Xn |
| \Cn="Hoofdstuktitel" | Voeg "Hoofdstuktitel" in de hoofdstuklijst in, met niveau n (zoals \Xn). De tekst wordt niet weergegeven op de pagina en dwingt geen pagina-einde af. Dit kan soms handig zijn om bijvoorbeeld een hoofdstukmarkering aan het begin van een inleiding op het hoofdstuk in te voegen. |
| \c | Centreer dit tekstblok; sluit met \c aan het begin van de regel |
| \r | Rechts uitvullen tekstblok; sluit met \r aan het begin van de regel |
| \i | Cursief blok; sluit af met \i |
| \u | Onderstreep blok; sluit met \u |
| \o | Overslag blok; afsluiten met \o |
| \v | Onzichtbare tekst; sluit af met \v (kan gebruikt worden voor commentaar) |
| \t | Blok inspringen. Begin aan het begin van een regel, sluit met \t aan het einde van een regel |
| \T="50%" | Laat het opgegeven percentage van de schermbreedte inspringen, in dit geval 50%. Als de huidige tekenpositie al voorbij de opgegeven schermlocatie is, wordt deze tag genegeerd. |
| \w="50%" | Sluit een horizontale regel in van een bepaald percentage breedte van het scherm, in dit geval 50%. Deze tag veroorzaakt een regeleinde ervoor en erna. De regel is gecentreerd. Het procentteken is verplicht. |
| \n | Schakel over naar het "normale" lettertype, dat door de gebruiker is opgegeven |
| \s | Schakel over naar stdFont; sluit met \s om terug te keren naar het normale lettertype |
| \b | Schakel over naar boldFont; sluit met \b om terug te keren naar het normale lettertype (verouderd; gebruik in plaats daarvan \B) |
| \l | Schakel over naar largeFont; sluit met \l om terug te keren naar het normale lettertype |
| \B | Markeer tekst als vet. In tegenstelling tot de tag \b, verandert \B het lettertype niet, dus u kunt grote vetgedrukte tekst gebruiken. U kunt \b en \B niet combineren in hetzelfde PML-bestand. |
| \Sp | Markeer tekst als superscript. Mag niet worden gemengd met andere stijlen zoals vet, cursief, enz. Voeg tekst in superscript toe met \Sp. |
| \Sb | Markeer tekst als subscript. Mag niet worden gemengd met andere stijlen, zoals vet, cursief, enz. Voeg subscripttekst toe met \Sb. |
| \k | Maak ingesloten tekst in kleine letters; sluit af met \k. Alle tekens tussen \k-tags (inclusief die met accenten) worden in hoofdletters gemaakt en worden weergegeven met een kleinere puntgrootte dan een normaal hoofdletter. |
| \\ | Vertegenwoordigt een enkele backslash |
| \aXXX | Voeg een niet-ASCII-teken in waarvan de Windows-1252-code decimaal XXX is. Zie de PML-tekentabel voor details. |
| \UXXXX | Voeg een niet-ASCII-teken in waarvan de Unicode-code hexadecimaal XXXX is. Zie de uitgebreide PML-tekentabel voor details. |
| \m="afbeeldingsnaam.png" | Voeg de benoemde afbeelding in. Zie het gedeelte over Afbeeldingen hieronder. |
| \q="#linkanchor"Enkele tekst\q | Verwijs naar een linkanker dat zich op een andere plek in het document bevindt. De tekenreeks na de ankerspecificatie en vóór de volgende \q is onderstreept of wordt op een andere manier weergegeven als een link bij het bekijken van het document. |
| \Q="linkanker" | Geef een koppelingsanker op in het document. |
| \- | Voeg een zacht koppelteken in. Een zacht koppelteken verschijnt alleen als het nodig is om een woord over een regel te breken. |
| \Fn="voetnoot1"1\Fn | Koppel de "1" aan een voetnoot waarvan de naam footnote1 is, getagd aan het einde van het PML-document. Zie het gedeelte over voetnoten en zijbalken hieronder. |
| \Sd="zijbalk1"Zijbalk\Sd | Koppel de tekst "Zijbalk" aan een zijbalk waarvan de naam zijbalk1 is, getagd aan het einde van het PML-document. Zie het gedeelte over voetnoten en zijbalken hieronder. |
| \Ik | Markeer als een referentie-indexitem. Omsluiten indexitem (en eventuele stijlcodes) met \I en \I.|


## Referenties

* [Palm Markup Language - Door MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Door MobileRead](https://en.wikipedia.org/wiki/E-reader)

