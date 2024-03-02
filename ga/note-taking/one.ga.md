{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "A hAON - Formáid Chomhaid Microsoft OneNote",
  "description": "Foghlaim faoi fhormáid comhaid AMHÁIN agus APIanna ar féidir leo comhaid AMHÁIN a chruthú agus a oscailt.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-gae"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad .ONE ann? ##

Cruthaítear comhad arna léiriú ag síneadh .ONE ag feidhmchlár Microsoft OneNote. Ligeann OneNote duit faisnéis a bhailiú trí úsáid a bhaint as an bhfeidhmchlár amhail is go bhfuil tú ag baint úsáide as do dhréachtchlár chun nótaí a ghlacadh. Is féidir gnéithe éagsúla a bheith i gcomhaid OneNote ar féidir iad a chur in áiteanna neamhsheasta ar leathanaigh doiciméad. Féadfaidh téacs, lámhscríbhneoireacht dhigiteach, agus réada a chóipeáiltear ó fheidhmchláir eile a bheith sna heilimintí seo lena n-áirítear íomhánna, líníochtaí agus gearrthóga ilmheán (fuaime/físeán). Cuireann Microsoft leagan ar líne de OneNote ar fáil anois mar chuid de Office365 inar féidir Nótaí a roinnt le húsáideoirí eile OneNote ar an idirlíon.

## .AON Sonraíochtaí Formáid Chomhaid ##

Soláthraíonn formáid comhaid OneNote bealach éifeachtach chun nótaí digiteacha a léiriú mar thacair ordlathacha de rannóga agus de leathanaigh. Tá ábhar atá sainithe ag an úsáideoir ar gach leathanach i struchtúr ar leith le léiriú ag an Formáid comhaid Document Object Model (DOM). Tá an tsamhail sonraí don fhormáid seo léirithe thíos.

### Forbhreathnú Struchtúr ###

Mar a léirítear sa tsamhail sonraí le haghaidh formáid comhaid OneNote, tá gnéithe éagsúla i ndoiciméad OneNote.

#### Roinn ####

Is éard atá i rannán an coimeádán is fearr i gcomhad OneNote a bhfuil gnéithe éagsúla ann freisin, mar shampla:

* Leathanaigh

* Meiteashonraí

* Airíonna


Áirítear le meiteashonraí agus airíonna ainm na rannóige, sainaithint na leathanaigh atá sa rannán, agus an t-ord ina bhfuil na leathanaigh sin le feiceáil. Tagraíonn an téarma rannóg do na leathanaigh go léir atá i rannán agus léiriú na sonraí sin i gcomhad stór athbhreithnithe OneNote®, a bhfuil síneadh ainm comhaid .one aige.

#### Leathanach ####

Tá ábhar atá sainithe ag an úsáideoir i ndoiciméad OneNote laistigh de leathanach. Áirítear ar fhaisnéis leathanaigh téacs, liostaí, táblaí, teidil leathanaigh, íomhánna agus clibeanna nótaí. Is éard atá i leathanach imlíne réada a gcuirtear an chuid is mó de na réada atá istigh leo. Is féidir ainm a thabhairt do gach leathanach le haghaidh léiriú brí agus is féidir rudaí a chur go díreach le leathanaigh freisin. Is féidir fo-leathanaigh a bheith ar leathanach eile i gcóras ordlathach.

#### Airíonna agus Tacair Airíonna ####

Is éard atá in inneachar OneNote airíonna, tacair airí agus réada sonraí comhaid. Is éard is tacar maoine ann ná bailiúchán maoine a léiríonn cineál éigin ábhair. Is éard atá i réad sonraí comhaid ná bloc de shonraí dénártha ina bhfuil pictiúir, comhaid leabaithe nó ábhar fuaime/físe.

#### Leabhar nótaí OneNote ####

Is éard is leabhar nótaí ann ná bailiúchán de chomhaid rannáin a stóráiltear san eolaire céanna. Úsáidtear cnuasach airíonna chun socruithe a shonrú ar nós ord na gcodanna laistigh den leabhar nótaí agus dath an leabhair nótaí.

### Struchtúr Comhad ###

NÍ MÓR do stór comhad athbhreithnithe tosú le struchtúr **Ceanntásc. Roinntear an chuid eile den chomhad i mbloic beart, áit a bhfuil méid agus struchtúr gach bloc sonraithe ag an réimse a thagraíonn dó. Is féidir teacht ar bhloc má tá tagairt dó sa struchtúr **Header**, nó má tá tagairt dó ag réimse i mbloc eile is féidir a rochtain. NÍ MÓR neamhaird a dhéanamh ar shonraí lasmuigh den struchtúr **Headder** agus ar aon bhloc insroichte.

Tá gach struchtúr ailínithe ar theorainneacha 1 beart. Sínítear gach slánuimhir mura sonraítear a mhalairt. Tá na réimsí go léir [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) mura sonraítear a mhalairt.

#### Ceanntásc ####

Cuimsíonn Ceanntásc comhad .ONE smután ina bhfuil aitheantais uathúla éagsúla agus réimsí chun faisnéis comhaid a léiriú mar seo a leanas:

`guidFileType (16 bytes):` GUID a shonraíonn cineál an chomhaid stórais athbhreithnithe. NÍ MÓR a bheith ar cheann de na luachanna ón tábla seo a leanas.


|Formáid Chomhaid|Luach
--- | --- |
|.amháin|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`GuidFile (16 bytes):` GUID a shonraíonn céannacht an chomhaid stórais athbhreithnithe seo. BA CHÓIR a bheith uathúil ar fud an domhain.

`guidLegacyFileVersion (16 beart):` NÍ MÓR a bheith {00000000-0000-0000-0000-00000000000} agus NÍ MÓR neamhaird a dhéanamh air.

`guidFileFormat (16 bytes):` GUID a shonraíonn gur comhad stórais athbhreithnithe é an comhad. NÍ MÓR é a bheith {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar an gcineál comhaid.

|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvCodeOldestThatHesWrittenToThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.


|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvCodeIs déanaíAtá ScríobhadhChunAn Comhad Seo (4 beart):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.

|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.

|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Struchtúr **FileChunkReference32** a NÍ MÓR luach fcrZero a bheith aige.

`fcrLegacyTransactionLog (8 beart):` Struchtúr **FileChunkReference32** nach mór a bheith ina fcrNil.

`cTransactionsInLog (4 beart):` Slánuimhir gan síniú a shonraíonn líon na n-idirbheart sa loga idirbheart. NÍ MÓR a bheith nialas.

`cbLegacyExpectedFileLength (4 bytes):` Slánuimhir gan síniú a NÍ MÓR a bheith ann, agus NÍ MÓR neamhaird a dhéanamh air.

`rgbPlaceholder (8 bytes):` Slánuimhir gan síniú a NÍ MÓR a bheith ann, agus NÍ MÓR neamhaird a dhéanamh air.

`fcrLegacyFileNodeListRoot (8 bytes):` Struchtúr **FileChunkReference32** nach mór a bheith ina fcrNil.

`cbLegacyFreeSpaceInFreeChunkList (4 byte):` Slánuimhir gan síniú a NÍ MÓR a bheith ann, agus NÍ MÓR neamhaird a dhéanamh air.

`fNeedsDefrag (1 byte):` NÍ MÓR neamhaird a dhéanamh.

`fRepairedFile (1 beart):` NÍ MÓR neamhaird a dhéanamh.

`fNeedsGarbageCollect (1 byte): `NÍ MÓR neamhaird a dhéanamh de.

`fHasNoEmbeddedFileObjects (1 beart):` Slánuimhir gan síniú a NÍ MÓR a bheith ann, agus NÍ MÓR neamhaird a dhéanamh de.

`guidAncestor (16 beart):` TREOIR a shonraíonn an réimse **Header.guidFile** den chomhad clár ábhair, tugtha ag an tábla seo a leanas:


|Formáid an Chomhaid Clár na nÁbhar|Suíomh an Chomhaid Clár na nÁbhar
--- | --- |
|Comhad Rannóige - .One|Tá an comhad clár na n-ábhar lonnaithe san eolaire céanna leis an gcomhad seo.
|Clár na nÁbhar Comhad - .onetoc2|Tá an comhad clár na nÁbhar suite i gcomhadlann tuismitheora an chomhaid seo.

Más é {00000000-0000-0000-0000-000000000000} an GUID, ní dhéanann an réimse seo tagairt do chomhad tábla ábhair.

`crcName (4 bytes):` Slánuimhir gan síniú a shonraíonn luach CRC ainm an chomhaid stórais athbhreithnithe seo. Is é an t-ainm ionadaíocht Unicode d'ainm an chomhaid lena síneadh agus carachtar nialasach breise ag an deireadh. Ríomhtar an CRC seo i gcónaí ag baint úsáide as an algartam CRC don chomhad .one, beag beann ar fhormáid comhaid an stórais athbhreithnithe seo.

`fcrHashedChunkList (12 beart):` Struchtúr **FileChunkReference64x32** a shonraíonn tagairt don chéad **FileNodeListFragment** i liosta smután hashed. Más fcrZero nó fcrNil luach an struchtúir **FileChunkReference64x32**, níl an liosta smután hashed ann.

`fcrTransactionLog (12 beart):` Struchtúr **FileChunkReference64x32** a shonraíonn tagairt don chéad struchtúr **TransactionLogFragment** i loga idirbheart. NÍ MÓR GAN luach an réimse **fcrTransactionLog** a bheith mar fcrZero” agus NÍ MÓR GAN bheith fcrNil”.

`fcrFileNodeListRoot (12 beart):` Struchtúr ** FileChunkReference64x32** a shonraíonn tagairt do liosta nód an chomhaid fhréamh. NÍ MÓR GAN luach an réimse **fcrFileNodeListRoot** a bheith mar fcrZero” agus NÍ MÓR GAN bheith fcrNil”.

`fcrFreeChunkList (12 beart):` Struchtúr **FileChunkReference64x32** a shonraíonn tagairt don chéad struchtúr **FreeChunkListFragment**. Más fcrZero nó fcrNil luach an struchtúir **FileChunkReference64x32**, ansin níl an liosta smután in aisce ann.

`cbExpectedFileLength (8 bytes):` Slánuimhir gan síniú a shonraíonn méid, i mbearta, an chomhaid stórais athbhreithnithe seo.

`cbFreeSpaceInFreeChunkList (8 bytes):` Slánuimhir gan síniú a CHÓIR méid, i mbearta, den spás saor atá sonraithe sa liosta smután saor a shonrú.

`guidFileVersion (16 bytes): `A GUID. Nuair atá luach an réimse **cTransactionsInLog** nó an réimse **guidDenyReadFileVersion** á athrú, NÍ MÓR **guidFileVersion** a athrú go TREOIR nua.

`nFileVersionGeneration (8 bytes):` Slánuimhir gan síniú a shonraíonn an líon uaireanta a d'athraigh an comhad. NÍ MÓR é a mhéadú nuair a athraíonn an réimse **guidFileVersion**.

`guidDenyReadFileVersion (16 bytes): `A GUID. Nuair a bhíonn inneachar reatha an chomhaid á athrú, gan struchtúr **Header** an chomhaid agus bloic stórála neamhúsáidte a áireamh, NÍ MÓR **guidDenyReadFileVersion** a athrú go GUID nua.

`grfDebugLogFlags (4 bytes):` NÍ MÓR a bheith nialas. NÍ MÓR neamhaird a dhéanamh.

`fcrDebugLog (12 beart):` Struchtúr ** FileChunkReference64x32** a NÍ MÓR luach a bheith aige fcrZero. NÍ MÓR neamhaird a dhéanamh.

`fcrAllocVerificationFreeChunkList (12 beart):` Struchtúr **FileChunkReference64x32** a NÍ MÓR a bheith mar fcrZero. NÍ MÓR neamhaird a dhéanamh.

`bnCreated (4 bytes):` Slánuimhir gan síniú a shonraíonn uimhir thógála an fheidhmchláir a chruthaigh an comhad stórais athbhreithnithe seo. BA CHÓIR neamhaird a dhéanamh.

`bnLastWroteToThisFile (4 beart):` Slánuimhir gan síniú a shonraíonn uimhir thógála an fheidhmchláir a scríobh an uair dheireanach chuig an stór athbhreithnithe seo. BA CHÓIR neamhaird a dhéanamh.

`bnOldestWritten (4 bytes):` Slánuimhir gan síniú a shonraíonn uimhir thógála an fheidhmchláir is sine a scríobh chuig an stór athbhreithnithe seo. BA CHÓIR neamhaird a dhéanamh.

`bnNewestWritten (4 beart):` Slánuimhir gan síniú a shonraíonn uimhir thógála an fheidhmchláir is nuaí a scríobh chuig an stór athbhreithnithe seo. BA CHÓIR neamhaird a dhéanamh.

`rgbReserved (728 bytes):` NÍ MÓR a bheith nialas. NÍ MÓR neamhaird a dhéanamh.

## Tagairtí ##

* [[MS-ONESTORE] - Formáid Chomhaid OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Vicipéid](https://ga.wikipedia.org/wiki/Microsoft_OneNote#References)


