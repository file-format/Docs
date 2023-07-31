{
  "date" : "2019-10-11",
  "keywords" :[ "emf-bestand", "emf-bestandsformaat", "wat is een emf-bestand", "bestand", "emf-voorbeeld", "emf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - verbeterde metabestandsindeling",
  "description":"Meer informatie over EMF-bestandsindeling en API's die EMF-bestanden kunnen maken en openen.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een EMF-bestand?

**Enhanced metafile format (EMF)** slaat grafische afbeeldingen apparaatonafhankelijk op. Metabestanden van EMF bestaan uit records van variabele lengte in chronologische volgorde die de opgeslagen afbeelding kunnen weergeven na parsering op elk uitvoerapparaat. Deze records met variabele lengte kunnen definities zijn van ingesloten objecten, opdrachten voor tekenen en grafische eigenschappen die essentieel zijn om de afbeelding nauwkeurig weer te geven. Wanneer een apparaat een EMF-metabestand opent met zijn eigen grafische omgeving, blijven de verhoudingen, afmetingen, kleuren en andere grafische eigenschappen van de originele afbeelding hetzelfde, ongeacht het platform van het openende apparaat.

## Korte geschiedenis ##

In 1990 ontwierp Microsoft een beeldbestandsformaat Windows Metafile ([WMF](/nl/image/wmf/)) voor Microsoft Windows. Windows-metabestanden hebben een 16-bits formaat dat enkele bitmapcomponenten kan bevatten. WMF kan bestaan uit vectorafbeeldingen en is bedoeld om overdraagbaar te blijven tussen verschillende toepassingen. In 1993 kondigde Win32/GDI de Enhanced Metafile (EMF) aan, een nieuwere versie met verbeterde flexibiliteit en schaalbaarheid. EMF wordt ook gebruikt als grafische taalopdrachten om de printerstuurprogramma's uit te voeren. Microsoft raadt nu het verbeterde metabestandsformaat (EMF) aan boven Windows-formaat (WMF). Toen Windows XP werd geïntroduceerd, werd de versie Enhanced Metafile Format Plus (EMF+) uitgebracht. Deze nieuwere versie vindt zijn weg door GDI+ API-aanroepen te serialiseren, en WMF/EMF registreert aanroepen naar GDI. Er bestaat een gzip-gecomprimeerde versie van EMF die bekend staat als EMZ.

## EMF Metabestand Formaat ##

Hieronder volgen de essentiële elementen van het verbeterde metabestandsformaat:

* Een EMR_HEADER (versie, grootte, de resolutie van de afbeelding bij het maken)
* Een tabel voor GDI-objecten
* Een gereserveerd palet (optioneel)
* Metabestandsrecords gerangschikt in matrixstructuur (eigenschapsinstellingen, gedefinieerde objecten, tekenopdrachten)
* EMR_EOF-record (laatste record in het EMF-metabestand)

## EMF-versies ##
* **Origineel**: de originele versie specificeert de record die nodig is om de originele afbeelding te behouden en apparaatonafhankelijk te houden. Ondersteunt bovendien het record met grafische objecten en opdrachten voor tekenen.
* **Versie 1**: de tweede versie van EMF verbeterde de flexibiliteit en apparaatonafhankelijkheid door het record voor pixelformaat en voorziening toe te voegen om de OpenGL-opdracht te gebruiken.
* **Versie 2**: de derde versie verbeterde de nauwkeurigheid door het metrische systeem toe te voegen om de oppervlakte-afstanden van het apparaat te meten, waardoor het record beter schaalbaar is.

## Verbeterde metabestandsrecords ##

Metafile-records zijn gerangschikt in de vorm van een array. Deze records hebben een ENHMETARECORD-structuur en zijn variabel in lengte. ENHMETARECORD specificeert gegevens die GDI-functies definiëren om een afbeelding te maken met behulp van een verbeterd metabestandsformaat. **ENHMETAHEADER** structuur is altijd de eerste record in dit formaat. Deze EMF-header bevat de volgende informatie.

Elk record van een verbeterd metabestand heeft in het begin twee leden van EMR (levert de basisstructuur). Het eerste lid herkent de GDI-functie (parameters worden gebruikt in record) die het type record bepaalt en staat bekend als iType. Het andere lid nSize definieert de grootte van elk record. Overige parameters (indien aanwezig) en aanvullende gegevens direct onder nSize gerangschikt. Onmiddellijk na de kop kan een optionele tekstbeschrijving worden weergegeven. In die tekstbeschrijving worden de naam van de foto en de auteur vastgelegd. Het palet waarvan de aanwezigheid een optie is, specificeert de kleuren die worden gebruikt bij het maken van verbeterde metabestanden. De andere records die worden gebruikt om de GDI-functie te specificeren die essentieel is bij het maken van afbeeldingen.

In elk metabestand moet ten minste één EMF-record aanwezig zijn. De verplaatsingsinformatie van het ene record naar het andere is afhankelijk van EMF-records, dus deze records moeten naast elkaar worden gerangschikt. Bij elk gegeven record in het metabestand behalve EOF_record, bepaalt de lengte van dat specifieke record om naar het volgende record te gaan.

## Verbeterde aanmaak van metabestanden ##

De functie **CreateEnhMetaFile** wordt gebruikt om een verbeterd metabestand te maken. Deze functieargumenten worden gebruikt voor afmetingen en opslag van afbeeldingen op schijf/geheugen. Verder vereist deze functie de afmeting van het apparaat waarin de afbeelding het eerst verscheen (verwezen apparaat) en de context van het referentieapparaat (DC). Dus de argumenten om deze DC af te handelen, moeten worden opgegeven bij het aanroepen van de functie **CreateEnhMetaFile**. De syntaxis van de functie is als volgt:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** handvat naar een referentieapparaat.

**lptoFilename:** Een verwijzing naar de bestandsnaam.

**lprc:** Aanwijzer naar ovale structuur specificeert de afbeeldingsafmetingen in mm.

**lpDesc:** een verwijzing naar een tekenreeks voor de titel van de afbeelding en de naam van de toepassing die de afbeelding heeft gemaakt.

## Verbeterde metabestandbewerkingen ##

Hieronder volgen taken die kunnen worden uitgevoerd met behulp van de handle naar een verbeterd metabestand.

* Weergeven en bewerken voor de opgeslagen foto.
* Maak verbeterde kopieën van metabestanden.
* Haal de kopie op van een EMF-header, optionele beschrijving en binaire versie van een verbeterd metabestand
* Recapituleert de kleuren in het palet.

## Grafische objecten ##

Bij teken- en schilderbewerkingen kunnen grafische objecten worden gemaakt door objectcreatierecords en kunnen ze worden opgeslagen voor verder gebruik. Een `EMR_SELECTOBJECT`-record kan deze grafische objecten ophalen met behulp van de context van het afspeelapparaat. Pennen, paletten, penselen, kleurruimten, lettertypen en standaardobjecten zijn enkele herbruikbare objecttypen.

## Byte-bestelling ##

Het Little-endian-formaat wordt gebruikt om gegevens op te slaan in metabestandsrecords.

## Versiebeheer ##

Het EMF-bestandsformaat is tweemaal herzien. De gewijzigde versies zijn origineel, extensie 1 en extensie 2. Uitgebreide versies hebben voorzieningen voor OpenGL-records en een optionele descriptor voor intern pixelformaat. Voor de weergegeven afmetingen is een meetfaciliteit in milliliter toegevoegd.

## Referenties ##

* [Enhanced-Format Metafiles | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Verbeterde metabestandsindeling en specificatie](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

