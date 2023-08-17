{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access Reports File",
  "keywords" :[ "mar", "mar-fil", "mar-filformat", "vad är åtkomstrapport", "åtkomstrapport", "microsoft åtkomstrapport"],
  "description":"Läs mer om filformatet Acess Report (MAR) som används av Microsoft Access-programvaran för att skapa en genväg eller länk till Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Vad är Access Report (MAR-fil)? ##
En fil som skapats av Microsoft Access som en genväg till rapporten sparas med filtillägget .mar. En **Microsoft Access-rapport** erbjuder ett sätt att formatera, visa och sammanfatta informationen i Microsoft Access-databasen. Dessa rapporter låter dig formatera dina data i en exakt och informativ layout för visning på skärm eller utskrift. Rapporten visar bara statisk data vilket innebär att vi inte kan ändra data i tabeller när vi tittar på Access-rapporten. Rapporten visar den senaste informationen när den öppnas.

## Microsoft Access Report (MAR) filformat

MAR-filformatet används av Microsoft Access-programvaran för att skapa en genväg eller länk till Microsoft Access Report som är ett databasobjekt som blir användbart när du behöver presentera informationen i din databas för någon av följande användningsområden:

- Visa en sammanfattning av data.
- Arkivera ögonblicksbilder av data.
- Visa detaljer om enskilda poster.
- Skapa etiketter.

## Delar av åtkomstrapport
Designen av en Access-rapport är uppdelad i olika sektioner som kan ses i designvyn. Följande tabell förklarar hur varje avsnitt fungerar och kan hjälpa dig att skapa rapporter.
| Avsnitt | Hur avsnittet visas när det skrivs ut | Där avsnittet kan användas |
---------|----|------|
| Rapporthuvud | I början av rapporten. | Använd rapporthuvudet för information som normalt kan visas på en försättssida, till exempel en logotyp, en titel eller ett datum. När du placerar en beräknad kontroll som använder funktionen Summaaggregat i rapporthuvudet, gäller den beräknade summan för hela rapporten. Rapporthuvudet skrivs ut före sidhuvudet. |
| Sidhuvud | Överst på varje sida. | Använd en sidhuvud för att upprepa rapporttiteln på varje sida. |
| Grupphuvud | I början av varje ny grupp av skivor. | Använd grupphuvudet för att skriva ut gruppnamnet. Till exempel, i en rapport som är grupperad efter produkt, använd grupphuvudet för att skriva ut produktnamnet. När du placerar en beräknad kontroll som använder funktionen Summaaggregat i grupphuvudet, är summan för den aktuella gruppen. Du kan ha flera grupprubrikavsnitt i en rapport, beroende på hur många grupperingsnivåer du har lagt till. Mer information om hur du skapar grupphuvuden och sidfötter finns i avsnittet Lägg till gruppering, sortering eller totaler. |
| Detalj | Visas en gång för varje rad i inspelningskällan. | Det är här du placerar kontrollerna som utgör huvuddelen av rapporten. |
| Gruppsidfot | I slutet av varje grupp av poster. | Använd en gruppsidfot för att skriva ut sammanfattningsinformation för en grupp. Du kan ha flera gruppsidfotsavsnitt i en rapport, beroende på hur många grupperingsnivåer du har lagt till. |
| Sidfot | I slutet av varje sida. | Använd en sidfot för att skriva ut sidnummer eller information per sida. |
| Rapportsidfot | I slutet av rapporten. Obs! I designvyn visas rapportsidfoten under sidfoten. I alla andra vyer (till exempel layoutvy eller när rapporten skrivs ut eller förhandsgranskas) visas rapportsidfoten ovanför sidfoten, precis efter den sista gruppsidfoten eller detaljraden på sista sidan. | Använd rapportsidfoten för att skriva ut rapportsummor eller annan sammanfattningsinformation för hela rapporten. |






## Referenser ##

- [Introduktion till rapporter i Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Designa rapporter i Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

