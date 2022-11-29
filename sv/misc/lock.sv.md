{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK File Format - Vad är en låsfil?",
  "description":"Läs mer om LOCK-filformatet och dess .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Vad är en LOCK-fil?

En **LOCK**-fil är en omdöpt fil som används av applikationer och operativsystem för att markera en fil eller någon enhet som låst. Detta talar om för andra applikationer att inte använda filen om den inte är fri från applikationen som använder den. I de flesta fall är dessa låsfiler tomma, men i andra fall kan de innehålla information relaterad till låset såsom egenskaper och inställningar.

Ibland används .lock-filen av Microsofts .NET Framework för att skapa **lockeed**-kopior av en databasfil. I ett sådant fall öppnas en kopia av databasfilen med tillägget .lock. Detta tillåter inte användaren att göra ändringar i filen medan den används av en annan användare.

## LÅS filformat - Mer information

En LOCK-fil skapas av varje applikation och dess filformat är specifikt för applikationen. Dessa låsfiler kan sparas i både text- och binärt filformat.

Närvaron av låsfiler förhindrar samtidig åtkomst av en resurs till flera filer som försöker få åtkomst till den resursen. En kopia av originalfilen skapas med filtillägget .lock som suffix till dess namn. Detta talar om för andra program att ha skrivskyddad åtkomst till filen. Till exempel kommer resource.dat att bli resource.data.lock.

För programmeringsspråket Ruby kan du stöta på filen **gemfile.lock**. Det är här Bundler registrerar de exakta versionerna som installerades. Således, när ett projekt/bibliotek flyttas till en annan maskin, kommer ett körande paket att titta på Gemfilen för den exakta relevanta versionen.

## Lås fil i Linux

Linux stöder två typer av fillås: rådgivande lås och obligatoriska lås.

* **Advisory Locks**: Typ av låsning som inte tillämpas. I det här fallet samarbetar deltagande processer med varandra för att explicit skaffa lås. Om detta inte är möjligt ignoreras rådgivande lås.

* **Obligatoriska lås**: Vid obligatorisk låsning upprätthåller operativsystemet fillåsningen genom att förhindra andra processer från att läsa eller skriva filen. Detta kräver inget samarbete mellan processerna.

obligatorisk låsning kräver inget samarbete mellan de deltagande processerna. När ett obligatoriskt lås är aktiverat på en fil, förhindrar operativsystemet andra processer från att läsa eller skriva filen.

## Referenser

* [GemFile och Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Låsning i Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

