{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MDMP fails — Windows Minidump faila formāts",
  "description": "Uzziniet par MDMP failu formātu un API, kas var izveidot un atvērt MDMP failus.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-lvp"
}
},
  "lastmod": "2022-08-19"
}

## Kas ir MDMP fails?

MDMP fails ir Microsoft Windows lietojumprogrammas atmiņas izspiedums, kas tiek izveidots, kad lietojumprogramma aizveras neparasti vai avarē. Tajā ir ietverta informācija un datu izgāztuves, ko var izmantot, lai atkļūdotu avārijas cēloni. MDMP faili ir lietojami lietojumprogrammās, kas izveidotas ar jebkuru platformu, piemēram, Java, C++, .NET un citas. Papildus MDMP,

Lietojumprogrammas, kas var atvērt MDMP failus, ietver Microsoft Visual Studio atkļūdotāju.

## MDMP faila formāts

MDMP faili tiek saglabāti diskā kā bināri faili, un tos var atvērt, izmantojot Microsoft Visual Studio atkļūdotāju. Tajā ir šāda informācija, kas palīdz noteikt avārijas iemeslu.

 * Sīkāka informācija par apturēšanas ziņojumu, tā parametriem un citiem datiem
 * Ielādēto draiveru saraksts
 * Procesora konteksts (PRCB) procesoram, kas pārtrauca darboties
 * Apturētā procesa informācija un kodola konteksts (EPROCESS).
 * Apstrādājiet informāciju un kodola kontekstu (ETHREAD) pavedienam, kas tika apturēts
 * Kodola režīma izsaukumu steks pavedienam, kas tika apturēts

Šī informācija palīdz noskaidrot notikušo, novērst problēmu un novērst tās atkārtošanos.

### Analizēt Minidump

Lai izveidotu atmiņas izdrukas failu, sistēmai Windows ir nepieciešams peidžeru fails sāknēšanas sējumā. Peidžeru fails tiek izveidots sāknēšanas sējumā, un tam jābūt vismaz 2 megabaitu (MB) lielam. Izgāztuves fails tiek izveidots, kad lietojumprogramma avarē. Otras problēmas gadījumā tiek izveidots otrs mazs atmiņas izgāztuves fails, bet iepriekšējais tiek saglabāts. Izgāztuves faila nosaukums ir atšķirīgs, lai izvairītos no pārrakstīšanas.

Windows saglabā visu atmiņas izdrukas failu sarakstu mapē %SystemRoot%\Minidump. Varat analizēt MDMP failus, palaižot tos programmā Visual Studio atkļūdotājs, kā norādīts tālāk norādītajās darbībās.

## Kā programmā Visual Studio atvērt MDMP failu?

Lai atvērtu MDMP failu programmā Visual Studio, var izmantot šādas darbības.

 * Programmas Visual Studio izvēlnē Fails izvēlieties Atvērt | Avārijas izgāztuve.
 * Pārejiet uz izgāztuves failu, kuru vēlaties atvērt.
 * Atlasiet Atvērt.

## Atsauce

* [Kā nolasīt mazo Windows izveidoto atmiņas izdrukas failu, ja notiek avārija](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fails)


