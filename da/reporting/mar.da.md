{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MAR - Microsoft Access Reports File",
  "keywords" : [ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"Lær om Acess Report (MAR) filformat, der bruges af Microsoft Access-software til at oprette en genvej eller et link til Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar-da",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Hvad er Access Report (MAR-fil)? ##
En fil oprettet af Microsoft Access som en genvej til dens rapport gemmes med filtypen .mar. En **Microsoft Access-rapport** tilbyder en måde at formatere, se og opsummere oplysningerne i Microsoft Access-databasen. Disse rapporter giver dig mulighed for at formatere dine data i et præcist og informativt layout til visning på skærm eller udskrivning. Rapporten viser blot de statiske data, hvilket betyder, at vi ikke kan ændre dataene i tabeller, når vi ser Access-rapporten. Rapporten viser de seneste data, når den åbnes.

## Microsoft Access Report (MAR) filformat

MAR-filformatet bruges af Microsoft Access-software til at oprette en genvej eller et link til Microsoft Access Report, som er et databaseobjekt, der bliver nyttigt, når du skal præsentere oplysningerne i din database til en af følgende anvendelser:

- Vis en oversigt over data.
- Arkiver snapshots af dataene.
- Vis detaljer om individuelle poster.
- Opret etiketter.

## Dele af adgangsrapport
Designet af en Access-rapport er opdelt i forskellige sektioner, som kan ses i Design-visningen. Følgende tabel forklarer, hvordan hvert afsnit fungerer og kan hjælpe dig med at oprette rapporter.
| Afsnit | Sådan vises afsnittet, når det udskrives | Hvor afsnittet kan bruges |
---------|----|------|
| Rapporthoved | I begyndelsen af rapporten. | Brug rapporthovedet til oplysninger, der normalt kan vises på en forside, såsom et logo, en titel eller en dato. Når du placerer et beregnet kontrolelement, der bruger funktionen Sum aggregeret i rapporthovedet, er den beregnede sum for hele rapporten. Rapporthovedet udskrives før sidehovedet. |
| Sidehoved | Øverst på hver side. | Brug en sidehoved til at gentage rapporttitlen på hver side. |
| Gruppeoverskrift | I begyndelsen af hver ny gruppe af poster. | Brug gruppeoverskriften til at udskrive gruppenavnet. I en rapport, der er grupperet efter produkt, skal du f.eks. bruge gruppeoverskriften til at udskrive produktnavnet. Når du placerer et beregnet kontrolelement, der bruger funktionen Sum aggregeret i gruppeoverskriften, er summen for den aktuelle gruppe. Du kan have flere gruppeoverskrifter i en rapport, afhængigt af hvor mange grupperingsniveauer du har tilføjet. For mere information om oprettelse af gruppehoveder og sidefødder, se afsnittet Tilføj gruppering, sortering eller totaler. |
| Detalje | Vises én gang for hver række i optagelseskilden. | Det er her, du placerer de kontroller, der udgør hoveddelen af rapporten. |
| Gruppesidefod | I slutningen af hver gruppe af poster. | Brug en gruppesidefod til at udskrive oversigtsoplysninger for en gruppe. Du kan have flere gruppesidefødder i en rapport, afhængigt af hvor mange grupperingsniveauer du har tilføjet. |
| Sidefod | I slutningen af hver side. | Brug en sidefod til at udskrive sidetal eller oplysninger pr. side. |
| Rapporter sidefod | I slutningen af rapporten. Bemærk: I designvisning vises rapportfoden under sidefoden. I alle andre visninger (f.eks. layoutvisning, eller når rapporten udskrives eller forhåndsvises), vises rapportfoden over sidefoden lige efter den sidste gruppesidefod eller detaljelinje på den sidste side. | Brug rapportfoden til at udskrive rapporttotaler eller andre oversigtsoplysninger for hele rapporten. |






## Referencer ##

- [Introduction to reports in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Designing Reports in Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

