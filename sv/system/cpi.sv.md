{
"datum":"2023-10-18",
   "keywords":[
"cpi",
"cpi-fil",
"cpi kodsida informationsfil",
"hur man öppnar en cpi-fil",
"fil",
"cpi filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"CPI-filformat - kodsidasinformationsfil",
   "description":"Läs mer om filformat för CPI-kodsidainformation och API:er som kan skapa och öppna CPI-filer.",
"linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
         "parent":"system"
}
},
"lastmod":"2023-10-18"
}

## Vad är en CPI fil?

En `.cpi`-fil, i kontexten av Microsoft Windows och DOS operativsystem, är vanligtvis **"Code Page Information File."** Dessa filer innehåller information om teckentabeller som används för textkodning och teckenuppsättningsmappningar. Kodsidor är viktiga för att visa och bearbeta text på olika språk och teckenuppsättningar.

I Windows och DOS-sammanhang används teckentabeller för att definiera hur tecken representeras och kodas i olika språk och regioner. Dessa teckentabeller bestämmer hur tecken lagras i minnet och visas på skärmen. Varje teckentabell har en unik identifierare och `.cpi`-filer lagrar information om dessa teckentabeller, inklusive detaljer som teckenmappningar och teckensnittsinformation.

`.cpi`-filer finns vanligtvis i Windows- eller DOS-systemkataloger och de spelar en avgörande roll för att göra det möjligt för operativsystemet att visa text korrekt för olika lokaler och teckenuppsättningar. De hjälper systemet att förstå hur man tolkar och återger tecken från olika språk och kodningar.

## Kodsida informationsfiler

Låt oss titta närmare på kodsidainformationsfiler (.cpi) och hur de fungerar inom ramen för MS-DOS och tidigare iterationer av Microsoft Windows:

1. **Teckenkodning och kodsidor**: Kodsidor är en avgörande del av hur text kodas och visas på datorn. De definierar teckenkodning för ett specifikt språk eller teckenuppsättning. Varje teckentabell tilldelar numeriska värden (kodpunkter) till tecken, vilket gör att datorn kan representera och visa dem. Exempelvis används teckentabell 437 ofta i USA och Västeuropa, medan teckentabell 850 används för Latin-1-kodning.
    







2. **Systeminitiering**: Under systeminitiering (när datorn startar), skulle MS-DOS och äldre versioner av Windows läsa `.cpi`-filer för att avgöra vilka teckentabeller som ska stödjas. Denna information var avgörande för textåtergivning, tangentbordsinmatning och teckenuppsättningskonverteringar.
    







3. **Skärm- och tangentbordsstöd**: Dessa filer ger information om hur tecken ska visas på skärmen och vilka teckenuppsättningar eller teckentabeller som ska stödjas för tangentbordsinmatning. Olika teckentabeller definierar olika teckenuppsättningar, så dessa filer hjälper operativsystemet att veta hur man hanterar användarinmatning och visar text korrekt.
    







4. **Lokalisering**: `.cpi`-filer är viktiga för lokalisering av operativsystem. De gör det möjligt för systemet att anpassa sig till olika språk, regioner och teckenuppsättningar, vilket gör det möjligt för användare över hela världen att använda MS-DOS eller Windows på sina föredragna språk.
    







5. **Flera `.cpi`-filer**: På datorer med flerspråkigt stöd kan du hitta flera `.cpi`-filer som motsvarar olika teckentabeller. Till exempel kan systemet ha "437.cpi" för USA, "850.cpi" för Latin-1, "852.cpi" för Centraleuropa och så vidare. Lämplig fil laddas baserat på användarens språk eller valda teckentabell.
    







6. **Teckensnittsinformation**: Förutom teckenmappningar kan dessa filer innehålla teckensnittsinformation som anger vilka teckensnitt som ska användas för varje teckentabell. Detta är viktigt för att rendera text i lämplig stil och storlek.
    







7. **Legacy Systems**: `.cpi`-filer var vanligare i äldre versioner av MS-DOS och Windows. Moderna Windows-versioner (som Windows 10 och senare) använder vanligtvis Unicode för textkodning, som stöder ett stort antal tecken och språk. Unicode förenklar textbehandling för flerspråkiga miljöer och är standard för modern programvara.

## Hur öppnar man filen CPI?

Att öppna en .CPI-fil (Code Page Information) är ingen typisk användaråtgärd och dessa filer är i allmänhet inte avsedda att öppnas manuellt. De används av operativsystem för att hantera textkodning och teckenuppsättningar och deras innehåll nås och används automatiskt av systemet.

Men om du är intresserad av att visa innehållet i .CPI-filen i informationssyfte kan du prova att öppna den med textredigerare eller hexadecimalvisare. Så här kan du försöka öppna .CPI-filen:

1. **Textredigerare**: Du kan använda textredigerare som Notepad (på Windows) eller vilken vanlig textredigerare som helst på andra operativsystem för att öppna och visa .CPI-fil. Tänk på att innehållet i .CPI-filer inte är avsett att vara läsbart för människor och du kan se serier av tecken som är svåra att tolka.
    







2. **Hexadecimal Viewer**: En hexadecimal viewer eller hex-redigerare kan användas för att öppna och inspektera innehållet i .CPI-filen i dess råa binära form. Hex-redigerare ger en mer detaljerad bild av filens data, vilket kan vara användbart om du försöker förstå dess struktur. Exempel på sådan programvara inkluderar HxD, Hex Fiend (för macOS) och 010 Editor.

## Andra CPI-filer

Här är andra filtyper som använder filtillägget **.cpi**.

**Video och system**
- [CPI - AVCHD-videoklippsinformation](/sv/video/cpi/)
- [CPI - Informationsfil för kodsida](/sv/system/cpi/)

## Referenser
* [Kodsida](https://en.wikipedia.org/wiki/Code_page)

