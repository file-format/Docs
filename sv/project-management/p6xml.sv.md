{
  "date" : "2021-04-16",
  "keywords" :[ "XML", "P6XML", "Fil", "Tillägg", "Filformat", "Projekt", "Management", "Primavera", "P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML - Primavera P6 Project",
  "description":"Läs mer om P6XML-filformat och API:er som kan skapa och öppna P6XML-filer.",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Vad är en P6XML fil? ##

Filtillägget P6XML har utmärkt läsbarhet, anpassningsbarhet och bred användning som gör det till det idealiska formatet. Primavera P6 Professional har funktionen att exportera och importera både [XER](/sv/project-management/xer)-filer och XML-filer. XML står för **Extensible Markup Language**. Detta allmänna format tillåter användare att dela projektinformation mellan Primavera P6-databaser. Projektdata kan enkelt lagras i en textfil genom XML-filen; detta gör det enklare för många program att utbyta data. Sådan data kan enkelt delas och hanteras av Primavera P6-användaren.

## Fördelar med ett P6XML-filformat ##

* Det är lätt för Primavera-användare att definiera vilka baslinjer som ska exporteras och importeras med hjälp av XML-filen
* XML-export kan innehålla alla projektdetaljerade handlingsplaner
* Alla användare som använder Primavera 6 som inte kan redigera, lägga till eller ta bort vissa globala dataobjekt, som aktivitetskoder, kalendrar och resurs kommer inte att kunna importera dem
* Utöver inställningarna för General och Project Security Profile som används av Primavera, kommer inte dataobjekt som kommer att påverka eller ändra data i databasen att importeras

## Exportera XML-filen från Primavera P6 ##

För att exportera P6 Professional-projekt och projektdata till en P6XML-fil, använd Oracle Primavera Cloud. Du kan ladda ner filen när den skapas från skrivbordsapplikationen P6 Professional och importera den till Primavera Cloud. Innan du oavbrutet utför exportprocessen bör du reglera om du är länkad till en P6 Professional-databas eller en P6 EPPM. Vissa funktioner i exportprocessen kan skilja sig beroende på din databas. Med P6 Specialized-inställningar med en P6 Proficient-databas, fungerar exportprocessen lokalt på ditt system. Med en P6 Professional-databas kan du enkelt exportera och öppna P6 XML-filen från en inställning på ditt system.

Här är några steg som beskriver exportprocessen:

* Öppna önskar Primavera P6-projekt
* Efter det väljer du Exportera på fliken Arkiv
* Välj "Primavera P6 – (XML)". Klicka sedan på Nästa
* Dubbelklicka på projektet som du ska exportera
* Välj trunkeringarna för sökvägen där du vill placera den exporterade filen och välj "Slutför".
* Välj alternativet för hur du vill spara filen
* Om layouter på projektnivå inte behövs med exportfilen är det viktigt att avmarkera markeringen till "Exportera alla layouter på projektnivå."
* Välj slutför, så får du en bekräftelse på XML-exporten

### Viktiga tips ###

* Närhelst man blir ansluten till en P6 EPPM-databas måste administratören skicka in URL:en för innehållskällan i P6 URL-fältet på sidan Allmänt i programinställningar i P6
* Det är bekvämt att exportera många projekt till en XML-fil
* Global data som allokeras till projektet exporteras
* Det är bekvämt att exportera XML-filer utan att ha tillgång till alla resurser
  


## Problem med att öppna filen P6XML? ##

Några vanliga problem som kan uppstå och orsaka att P6XML-formatet inte fungerar är följande:

* Avsaknad av stödprogramvara
* Korrupt fil
* Infekterad fil på grund av virus
* P6XML-beskrivningen raderades av misstag från Windows-registret
* Ingen åtkomsträtt i systemet för att öppna filerna
* Föråldrad enhet i ditt system
* Filtillägget döps om
 

## Referenser ##

* [Oracle - P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_eppm_xml_import_guide/190894.htm)

