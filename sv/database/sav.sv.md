{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "tillägg", "sav fil", "sav filformat", "Databasfiltyp", "Databasfilformat", "vad är en sparafil" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om SAV-filformat och API:er som kan skapa och öppna SAV-filer.",
  "title" :"SAV - SPSS-datafil",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Vad är en SAV-fil?
SAV-fil är en datafil skapad av Statistical Package for the Social Sciences (SPSS), som är en applikation som ofta används av marknadsforskare, hälsoforskare, undersökningsföretag, myndigheter, utbildningsforskare, marknadsföringsorganisationer, dataminers för statistisk analys. SAV sparas i ett proprietärt binärt format och består av en datauppsättning såväl som en ordbok som representerar datauppsättningen, sparar data i rader och kolumner.

## SAV-filformat
SAV-filformatet har blivit relativt stabilt, men vi kan inte säga att det är statiskt. Bakåt- och framåtkompatibilitet är valfritt tillgängligt vid behov, men underhålls inte ordentligt. Data i en SAV-fil är kategoriserad i följande avsnitt:

### Filhuvud
Den består av 176 byte. De första 4 byten indikerar strängen **$FL2** eller **$FL3** i teckenkodningen som används för filen. De tre sista byten representerar att data i filen är komprimerad med **ZLIB**. Nästa 60-byte sträng börjar **@(#) SPSS DATA FILE** och bestämmer även operativsystemet och SPSS-versionen som skapade filen. Rubriken fortsätter sedan med sexsiffriga fält, som innehåller antalet variabler per observation och en sifferkod för komprimering, och avslutas med teckendata som anger datum och tid för skapande och en filetikett.
### Variabel deskriptorposter
Posten innehåller en fast sekvens av fält, som klassificerar typen och namnet på variabeln tillsammans med formateringsinformation som används av SPSS. Varje variabelpost kan valfritt innehålla en variabeletikett på upp till 120 tecken och upp till tre specifikationer för saknade värden.
### Värdeetiketter
Värdeetiketterna är valfria och lagras i par av poster med heltalstaggar 3 och 4. Den första posten, som är tagg 3, har en sekvens av fältpar, där varje par innehåller ett värde och den tillhörande värdeetiketten. Den andra posten som är tag 4, representerar vilka variabler uppsättningen värden/etiketter gäller.
### Dokument
Enstaka eller flera poster med heltalstagg 6. Valfri dokumentation. innehåller 80 tecken rader.
### Tilläggsposter
Enstaka eller flera poster med heltalstagg 7. Tilläggsposter ger information som säkert kan ignoreras, men som bevaras i många situationer gör det möjligt för filer skrivna av nyare programvara att bevara bakåtkompatibilitet. Tilläggsposter har heltalsundertyptaggar.
### Ordboksterminator
Spela bara in med heltalstagg 999. Den skiljer ordbok från dataobservationer.
### Dataobservationer
Det anses vara data i observationsordning, t.ex. alla variabelvärden för den första observationen, följt av alla värden för den andra observationen, etc. Datapostens format varierar beroende på komprimeringskoden i filhuvudposten. Datadelen av en .sav-fil kan okomprimeras:
- **kod 0**: komprimerad av bytekod
- **kod 1**: komprimerad med ZLIB-komprimering
 







## Referenser ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

