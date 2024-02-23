{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA-bestand - xdelta differentieel bestand - Wat is een .xdelta-bestand en hoe kan ik het openen?",
  "description" : "Leer meer over xdelta Differential File en hoe u het kunt openen.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-nl",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Wat is een XDELTA-bestand?

Het XDELTA-bestandsformaat bevat de binaire verschillen tussen twee andere bestanden en wordt gegenereerd door de xdelta-tool, een opdrachtregelprogramma voor delta-codering, waarbij de verschillen tussen twee bestanden worden berekend en die verschillen in een compact formaat worden gecodeerd. XDELTA-bestanden slaan binaire gegevens op die veranderingen of verschillen tussen het originele bestand en het bijgewerkte bestand vertegenwoordigen. De binaire gegevens in een XDELTA-bestand vertegenwoordigen de wijzigingen die nodig zijn om het ene bestand (het origineel) om te zetten in een ander bestand (de bijgewerkte of gepatchte versie).

XDELTA-bestanden worden vaak gebruikt in de gaminggemeenschap om aanpassingen (mods) voor videogames te distribueren. Deze mods kunnen van alles omvatten, van cosmetische veranderingen tot aanzienlijke veranderingen in de gameplay-mechanica. Met XDELTA-bestanden kunnen gebruikers deze wijzigingen toepassen op hun game-installaties door de originele gamebestanden te patchen met de wijzigingen die zijn gespecificeerd in het XDELTA-bestand.

## xdelta

`xdelta` is een opdrachtregelprogramma dat wordt gebruikt voor delta-codering en -decodering; het wordt voornamelijk gebruikt voor het maken en toepassen van binaire patches, vaak delta patches of xdelta patches genoemd, tussen twee bestanden; deze patches vertegenwoordigen verschillen tussen het originele bestand en de gewijzigde of bijgewerkte versie, waardoor een efficiënte distributie van updates mogelijk is, vooral in scenario's waarin de bandbreedte of opslagruimte beperkt is.

Hier is een kort overzicht van de belangrijkste functionaliteiten van `xdelta`:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` wordt vaak gebruikt in verschillende scenario's, zoals het distribueren van software-updates, het patchen van videogames en het updaten van systeembestanden op ingebedde apparaten of netwerkapparaten. Het biedt een flexibele en efficiënte manier om bestandsupdates te beheren en tegelijkertijd het bandbreedtegebruik en de opslagvereisten te minimaliseren.

## xdeltaui

xdeltaui is een grafische gebruikersinterface (GUI)-applicatie voor het beheren en toepassen van XDELTA-patches. xdelta gui biedt een gebruiksvriendelijke interface waarmee gebruikers kunnen communiceren met XDELTA-bestanden en deze kunnen toepassen op overeenkomstige originele bestanden, waardoor ze effectief kunnen worden gepatcht of bijgewerkt.

In tegenstelling tot de opdrachtregelversie van xdelta, die werkt via op tekst gebaseerde opdrachten, biedt xdeltaui een meer intuïtieve manier om met XDELTA-bestanden om te gaan, vooral voor gebruikers die niet bekend zijn met opdrachtregelinterfaces of de voorkeur geven aan grafische hulpmiddelen.

Met xdeltaui kunnen gebruikers doorgaans taken uitvoeren zoals het selecteren van het originele bestand, het selecteren van het XDELTA-patchbestand en het toepassen van patch om een bijgewerkt bestand te genereren. Dit kan met name handig zijn voor het installeren van mods of updates voor videogames of andere softwaretoepassingen.

## xdelta downloaden

Op Linux-systemen kunt u pakketbeheerders zoals `apt`, `yum` of `dnf` gebruiken om `xdelta` te installeren. Op Ubuntu kunt u bijvoorbeeld de volgende opdracht gebruiken:

```
sudo apt-get install xdelta3
```

## Hoe xdelta te gebruiken

Om `xdelta` te gebruiken, moet u doorgaans deze algemene stappen volgen:

1.  **Downloaden en installeren**: Zorg er eerst voor dat `xdelta` op uw systeem is geïnstalleerd. U kunt het downloaden van de officiële website, pakketbeheerders of andere vertrouwde bronnen.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Een patch maken**:
    
- Open uw opdrachtregelinterface (terminal of opdrachtprompt).
- Gebruik de opdracht `xdelta` met de juiste opties om een patch te maken. De basissyntaxis is:
               
```
xdelta-delta<original_file><updated_file><patch_output_file>
```
        
Vervang `<original_file> ` met pad naar origineel bestand, `<updated_file> ` met pad naar bijgewerkt bestand, en `<patch_output_file> ` met de gewenste naam voor het patchbestand.
- Voorbeeld:
               
```
xdelta delta origineel_bestand bijgewerkt_bestand patch.xdelta
```
        
4.  **Een pleister aanbrengen**:
    
- Zorg ervoor dat u het originele bestand en het patchbestand bij de hand heeft.
- Open uw opdrachtregelinterface.
- Gebruik de opdracht `xdelta` met de juiste opties om patch toe te passen. De basissyntaxis is:
        
      
```
xdelta-patch<original_file><patch_file><output_file>
```
        
Vervang '<original_file> ` met pad naar origineel bestand, `<patch_file> ` met pad naar patchbestand, en `<output_file> ` met de gewenste naam voor het uitvoerbestand.
- Voorbeeld:
                
```
xdelta patch origineel_bestand patch.xdelta bijgewerkt_bestand
```
        
5.  **Hulp bekijken**: Als u hulp nodig heeft bij specifieke opties of opdrachten, kunt u de opdracht `xdelta` gebruiken met de optie `--help` om gebruiksinformatie en beschikbare opties weer te geven.
    
## Hoe een XDELTA-bestand te openen

XDELTA-bestanden zijn niet bedoeld voor directe opening. Als u een XDELTA-patch op een game of een ander bestand wilt toepassen, heeft u de mogelijkheid om xdelta te gebruiken, dat compatibel is op meerdere platforms, of xdelta UI, speciaal ontworpen voor Windows-gebruikers.

## Referenties
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


